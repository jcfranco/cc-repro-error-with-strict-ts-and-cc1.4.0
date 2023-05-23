# Repro case for error caused when building with TS (strict) and calcite-components@1.4.0

## Steps to repro

1. clone repo
1. run `npm i && npm start`
1. notice the following error:

```
node_modules/@esri/calcite-components/dist/types/components.d.ts:5077:15 - error TS2320: Interface 'HTMLCalciteMenuElement' cannot simultaneously extend types 'CalciteMenu' and 'HTMLStencilElement'.
  Named property 'role' of types 'CalciteMenu' and 'HTMLStencilElement' are not identical.

5077     interface HTMLCalciteMenuElement extends Components.CalciteMenu, HTMLStencilElement {
                   ~~~~~~~~~~~~~~~~~~~~~~


Found 1 error in node_modules/@esri/calcite-components/dist/types/components.d.ts:5077
```
