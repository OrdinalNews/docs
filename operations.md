# Operations

## Posting News

News is inscribed as an [Ordinal inscription](https://docs.ordinals.com/inscriptions.html) with only a Bitcoin transaction.

To create a new post using the Ordinal News Standard, create an inscription following the convention below. [(inspired by Sats Names)](https://docs.sats.id/sats-names/protocol-spec)

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

{% hint style="info" %}
The syntax used above helps indexers process the information correctly and consistently. This is an example of the bare minimum requirements, and more information can be added using the Experimental Syntax outlined below.
{% endhint %}

### Experimental Syntax ⚠️

Anyone is welcome to include extra information in the inscription as optional parameters.

These can be added and adopted as the standard evolves, and as a result, new layers can be built on top of the standard itself.

| Key           | Required? | Description                                            |
| ------------- | --------- | ------------------------------------------------------ |
| url           | No        | URL: supporting link for the content                   |
| body          | No        | Body: supporting text as either plain text or markdown |
| author        | No        | Author: common identifier for who is posting content   |
| authorAddress | No        | Author Address: the address of the poster              |
| signature     | No        | Signature: proof that the author address is the poster |

{% hint style="info" %}
To discuss optional fields, share an implementation, or contribute any other ideas to the standard, please [visit GitHub and create an issue](https://github.com/OrdinalNews/docs/issues)!
{% endhint %}

Below is a post example with extra syntax:

```json
{
  "p": "ons",
  "op": "post",
  "title": "The Times 03/Jan/2009 Chancellor on brink of second bailout for banks.",
  "url": "https://mempool.space/block/000000000019d6689c085ae165831e934ff763ae46a2a6c172b3f1b60a8ce26f",
  "author": "whoabuddy.sats",
  "body": "Fourteen years ago, the Bitcoin network stored it's very first block, inscribed with the insightful text that the current financial systems were unsustainable. The answer lies in a peer to peer digital currency and payment network created, maintained, and used by a sovereign collective. Now is the time to get involved!"
}
```
