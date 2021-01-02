# Token

## How is my API usage calculated?

All plans can generate as many API tokens as you need. The sum of all token usage counts towards the call limit. For example, a pro plan with two tokens with 20k & 25k calls still has 5k calls remaining in the day.

## How can I create an API token?

Once you create an account, there should be a button to generate your first API token. You can create more tokens by pressing the + button in the table header. You can edit details for each token in the list.

## How do I use the development token?

Paid plans are given a separate token with 4k calls that doesn't count against their plan limit. Because the token usage is capped, it should not be used for any production systems.

## What happens if I hit the call limit?

Currently, the API will return a 429 error code for the remainder of the day. The count is reset at 00:00Z every day. I'm currently working on an opt-in option to allow overage billing instead of cutting access. It should be available by the end of January 2021.

## What happens if I refresh an API token?

Because each API token has a private ID internally, you can refresh a token's value as much as you want. You won't lose any usage data.

## How do I view my token usage?

You can view the last 30 days of token usage by selecting the chart icons in the token list. Press the header icon to display all tokens or each row for a single token.