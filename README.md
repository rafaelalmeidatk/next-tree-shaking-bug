## How to reproduce:

```bash
git clone https://github.com/rafaelalmeidatk/next-tree-shaking-bug
cd next-tree-shaking-bug
yarn
yarn build-and-analyze
```

The result should be normal. Open the file `packages/ui-lib/components/BigText/index.tsx` and uncomment the last line. Run the `build-and-analyze` command again and you should see a huge increase in the bundle, but the `BigText` component isn't imported anywhere.

> Repo based from https://github.com/LukasBombach/tree-shakable-component-library
