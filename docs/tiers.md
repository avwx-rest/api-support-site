# Feature Tiers

### What plans do you offer?

You'll find a list of available plans along with their features, price, and call limit on the [account portal].

### Do you have any options for open-source projects?

There is an open-source plan available which mirrors the free plan but with a higher call limit. If you are the creator or maintainer of a project currently using AVWX, [email me] with a link to your project repo.

### Can I switch my plans after subscribing?

You can switch your plan at any time. Your API tokens do not need to be changed when switching to another plan. It may take up to 15 minutes for the plan change to take effect in the API due to caching.

### What happens if I hit the call limit?

Currently, the API will return a 429 error code for the remainder of the day. The count is reset at 00:00Z every day. I'm currently working on an opt-in option to allow overage billing instead of cutting access. It should be available by the end of January 2021.

### What if I need a higher call limit?

If you regularly need more than what the Enterprise plan provides, [email me] so we can make a custom plan (features, calls, pricing) that fits your specific use-case.

[email me]: mailto:avwx@dupont.dev "Email Me"
[account portal]: https://account.avwx.rest "AVWX Account Home"