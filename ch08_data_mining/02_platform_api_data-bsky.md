# Data From the Bluesky API

We've been accessing Bluesky through Python and the "atproto" code library. The atproto code library works by sending requests across the internet to Bluesky, using what is called an "[application programming interface](https://en.wikipedia.org/wiki/API)" {cite:p}`API2023a` or API for short. APIs have a set of rules for what requests you can make, what happens when you make the request, and what information you can get back.

If you are interested in learning more about what you can do with atproto and what information you can get back, you can look at the official documentation for those. But be warned they are not organized in a friendly way for newcomers and take some getting used to to figure out what these documentation pages are talking about.

So, if you are interested, you can look at [the atproto library documentation](https://atproto.blue/en/latest/readme.html) {cite:p}`siamionau_getting_2024` to find out what the library can do (again, not organized in a beginner-friendly way). You can learn a little more about [what actions the client can do here](https://atproto.blue/en/latest/atproto_client/client.html) {cite:p}`siamionau_client_2024`. You can also reference some [official example programs](https://github.com/MarshalX/atproto/tree/main/examples) {cite:p}`noauthor_atprotoexamples_2025`.

You can also look up information on the data that you can get from the AT Protocol API (apart from any programming languages) by looking at the [AT Protocol API Documentation](https://atproto.com/) {cite:p}`noauthor_at_2025`. 

The AT Protocol API lets you access a lot of the data that Bluesky tracks (since Bluesky is a more open social media protocol), but Bluesky probably track much more than they let you have access to (like what other social media platforms do).
