# Operations

## Posting News

Posting is avaiable to anyone that can transact on Bitcoin. News can be inscribed as ordinals with only a Bitcoin transaction.

To create a new post within the Ordinal News Standard simply inscribe an ordinal containing the following syntax.

```
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
