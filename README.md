# Operations

## Posting News

Posting news is available to anyone that can transact on Bitcoin. News can be inscribed as ordinals with only a Bitcoin transaction.

To create a new post within the Ordinal News Standard simply inscribe an ordinal containing the following syntax. [_(inspired by Sats Names)_](https://docs.sats.id/sats-names/operations)__

```json
{
  "p": "ons",
  "op": "post",
  "title": "The Times 03/Jan/2009 Chancellor on brink of second bailout for banks."
}
```

| Key   | Required? | Description                                                       |
| ----- | --------- | ----------------------------------------------------------------- |
| p     | Yes       | Protocol: identifies this as an Ordinal News Standard inscription |
| op    | No        | Operation: helps indexers compute correct state                   |
| title | Yes       | Title: headline for the news to be                                |

Note: Following the syntax above is required to help indexers process the information correctly and consistently. Unlike Sats Names, the protocol field is required to differentiate news posts from normal Ordinal inscriptions, and the title is the only other required field.

### Experimental Syntax ⚠️

Anyone is welcome to include more information in the ordinal inscription. More optional parameters will likely be added and adopted as the standard evolves, but more exploration and testing needs to be done before it becomes a recommended practice.

| Key    | Required? | Description                                            |
| ------ | --------- | ------------------------------------------------------ |
| url    | No        | URL: supporting link for the content                   |
| body   | No        | Body: supporting text as either plain text or markdown |
| author | No        | Author: common identifier for who is posting content   |

Below is a post example with extra syntax:

```json
{
  "p": "ons",
  "op": "post",
  "title": "The Times 03/Jan/2009 Chancellor on brink of second bailout for banks."
  "url": "https://mempool.space/block/000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f",
  "body": "Fourteen years ago, the Bitcoin network stored it's very first block, inscribed with the insightful text that the current financial systems were unsustainable. The answer lies in a peer to peer digital currency and payment network created, maintained, and used by a sovereign collective. Now is the time to get involved!",
  "author": "whoabuddy.sats"
}
```
