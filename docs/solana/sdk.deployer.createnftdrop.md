---
slug: /sdk.deployer.createnftdrop
title: Deployer.createNftDrop() method
hide_title: true
displayed_sidebar: solana
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

## Deployer.createNftDrop() method

Create a new NFT drop program

**Signature:**

```typescript
createNftDrop(metadata: NFTDropContractInput): Promise<string>;
```

## Parameters

| Parameter | Type                 | Description                          |
| --------- | -------------------- | ------------------------------------ |
| metadata  | NFTDropContractInput | the metadata of the nft drop program |

**Returns:**

Promise&lt;string&gt;

- the address of the new nft drop program

## Example

```jsx
const metadata = {
  name: "NFT",
  symbol: "NFT",
  price: 0,
  sellerFeeBasisPoints: 0,
  itemsAvailable: 5,
};

const address = await sdk.deployer.createNftDrop(metadata);
```
