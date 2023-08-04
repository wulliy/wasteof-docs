# api

this category contains all of the documentation that you'll probably want for wasteof.money's APIs.

# notes
- most of these endpoints require you to provide a token in the `Authorization` header when making any requests to them.
- any endpoint that has `__data.json` appended to the end of the URL is equivalent to making a request to the same URL with the `Accept` header set to `application/json`. note that this **only** works for beta and alpha and, when used with alpha, it'll return JSON that won't be very human-readable. but, this can be easily solved with something like [devalue](https://github.com/Rich-Harris/devalue).
- the beta API is [mainly used internally and, as such, could change at any moment without notice](https://wasteof.money/posts/629eef086586aae544597fac).
- the [current wasteof2 API](https://api.wasteof.money) is considered to be legacy and is planned to be rewritten soon, so stay on the look out for when that happens.
- as of the time of writing this (08/04/2023), tokens don't expire until you log out. this is due to a flaw with how the backend handles sessions.