# Operations

## Posting News

News is inscribed as an [Ordinal inscription](https://docs.ordinals.com/inscriptions.html) with only a Bitcoin transaction.

To create a new post using the Ordinal News Standard, create an inscription following the convention below [(inspired by Sats Names)](https://docs.sats.id/sats-names/protocol-spec).

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

Below is an example with extra syntax, from [Reporter Can't Give Example Of "Hateful Speech" After Blaming Elon For It](https://inscribe.news/view-news?id=1159706).

```json
{
  "p": "ons",
  "op": "post",
  "title": "Reporter Can't Give Example Of \"Hateful Speech\" After Blaming Elon For It",
  "url": "https://www.piratewires.com/p/bbc-journalist-elon-hateful-speech",
  "author": "Mike Solana (@micsolana), Brandon Gorrell (@brandongorrell)",
  "body": "[](https://substackcdn.com/image/fetch/f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25dc0074-71c2-4eb9-a193-03060348ad96_2970x1618.png)\n\n![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F25dc0074-71c2-4eb9-a193-03060348ad96_2970x1618.png)\n\nThis is what we came for.\n\nLast night, ...truncated... and truly believe he is, the enemy. But last night, rather than apologize for crimes he never committed, he simply asked a follow-up question.\n\nThis is the way.\n\n-SOLANA\n\n_Interview paraphrased for clarity and flow before the blockquote._"
}
```

These fields can be used to display additional information, apply formatting, and enable new functionality for any front-end that consumes the data.

Another example [from Sigle](https://sigle.io), a blogging platform that gives you the option to publish articles as news inscriptions, with signature verification for the author's address: [Can You Achieve Immortality On Bitcoin?](https://inscribe.news/view-news?id=593292)

```json
{
  "p": "ons",
  "op": "post",
  "id": "QI41ThxSpKGyN1YJcFpGj",
  "author": "21milbtc.btc",
  "authorAddress": "SP3BCZN307DECNR5PRMV6HY4P37AJ9N48JP0VE547",
  "title": "Can You Achieve Immortality On Bitcoin?",
  "body": "<p>Well, it seems like the uproar over ordinals has died down a bit and is fading into the background of the Bitcoin ecosystem. Ordinals are here to stay and will not be going away any time soon. For good or bad, it is what it is. The rules allow it, and that basically the end of the story.</p><p>I personally don’t have a strong opinion on ordinals one way or other other. I think it’s kinda cool that you can inscribe data to the Bitcoin blockchain and have it live there forever. Think of the application that it could be used for. Imagine if Wikileaks had access to Ordinal software when they exposed government misconduct.</p><p>What ordinals can do to improve government transparency is genuinely off the charts, and I am looking forward to the many use cases that it unlocks. I had an epiphany yesterday, and it hit me out of nowhere. Ordinals are the closest thing that we will get to immortality in this life. Sure, it sounds crazy and a little out there, but when you think about it briefly, you will understand what I am trying to say.</p><p>We all have a finite amount of time before we die. This is a simple fact of life. We are born, we live, and we die. What we do between birth and death is up to us. Do you ever stop to think about if people will think about you when you are gone? Sure, your family and friends will miss you, but after a while, memories fade, and people also start to die off. In 50-100 years, no one will be left to remember your laugh, smile, thoughts, and even what you looked like.</p><p>The memory of you fades into the ether as it has for millions of people born before us. No one remembers the day laborer back in 1775 or the blacksmith from 350 AD because the technology didn’t exist back then to keep their memory alive.</p><p>This is why I think Ordinials is such a unique use of the Bitcoin blockchain. For the first time in history, you can inscribe the memory of YOU into the annuls of history FOREVER. Regular plebs like us can live on forever and essentially become immortal.</p><p>When you inscribe a satoshi with your image, thoughts, a love note to your wife or husband, or whatever else you want people to remember, it is being etched into the most secure blockchain ever created. No one can erase you off the face of the Earth.</p><p>No one knows for sure what happens after death, but one thing is knowable in this lifetime. Bitcoin is immutable and will endure for decades, if not thousands of years, into the future. I believe that when the history of Bitcoin is studied, the creation of Ordinals will mark a distinct epoch in the evolution of Bitcoin.</p><p>Thanks for reading!</p><p>If you want to support my blog, follow me on <a target=\"_blank\" rel=\"noopener noreferrer nofollow\" href=\"https://twitter.com/BTC_Apostle\">Twitter</a> and <a target=\"_blank\" rel=\"noopener noreferrer nofollow\" href=\"https://app.sigle.io/21milbtc.btc\">Sigle</a>!</p><p>You can also help out by sending sats or STX!</p><p><strong><em>Bitcoin: bc1q2sy7thucye5qphpr4upz34l99yl5m33ggrtjdl</em></strong></p><p><strong><em>Stacks: SP3BCZN307DECNR5PRMV6HY4P37AJ9N48JP0VE547</em></strong></p>",
  "url": "https://app.sigle.io/21milbtc.btc/QI41ThxSpKGyN1YJcFpGj",
  "signature": "99562038d5453c4e3c1aace7e3b08b547a046730224805b0fc13c49c495271e833c2c1e9dfb8800c9e7a9305b56df165e1f6df1c2a3559ebe7bffcf5765cf02200"
}
```
