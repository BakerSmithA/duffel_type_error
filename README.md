# Duffel type error example

To replicate, run:

```
npm i
npm run build
```

You should see

```
node_modules/@duffel/api/dist/typings.d.ts:1288:32 - error TS2307: Cannot find module 'types' or its corresponding type declarations.

1288     import { OrderSlice } from 'types';
                                    ~~~~~~~

node_modules/@duffel/api/dist/typings.d.ts:3767:36 - error TS2307: Cannot find module 'types' or its corresponding type declarations.

3767     import { PaginationMeta } from 'types';
                                        ~~~~~~~

node_modules/@duffel/api/dist/typings.d.ts:3921:12 - error TS1038: A 'declare' modifier cannot be used in an already ambient context.

3921     export declare class Airlines extends Resource {
                ~~~~~~~

```

Can be fixed using 

```
"skipLibCheck": true
```

in `tsconfig.json`
