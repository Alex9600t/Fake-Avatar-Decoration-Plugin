# Fake Avatar Decoration

## Simple plugin to add a fake Avatar decoration visible to all users who have the plugin installed.

### Examples:
![deco 0](https://github.com/Alex9600t/public-data/blob/main/fad/RM_img_0.png?raw=true)
![deco 1](https://github.com/Alex9600t/public-data/blob/main/fad/RM_img_1.png?raw=true)

### How to install?
1) Read [this page](https://docs.vencord.dev/installing) and follow all the instructions.
2) Clone the repository:
```sh
cd src
git clone https://github.com/Alex9600t/Fake-Avatar-Decoration-Plugin userplugins/fakeAvatarDecoration
```
3) Rebuild vencord:
```sh
pnpm build
pnpm inject
```
4) 
> [!IMPORTANT]
> In the file ***Vencord/src/main/csp/index.ts***, add the following value to the end of the ***CspPolicies*** variable:
> ```ts
> "vcfad.vercel.app": ImageAndCssSrc
> ```
>
> Example:  
> Before:
> ```ts
> export const CspPolicies: PolicyMap = {
>    "http://localhost:*": ImageAndCssSrc,
>    "http://127.0.0.1:*": ImageAndCssSrc,
>    "localhost:*": ImageAndCssSrc,
>    // ...
>     "usrbg.is-hardly.online": ImageSrc, // USRBG API
>     "icons.duckduckgo.com": ImageSrc, // DuckDuckGo Favicon API (Reverse Image Search)
> }
> ```
> After:
> ```ts
> export const CspPolicies: PolicyMap = {
>    "http://localhost:*": ImageAndCssSrc,
>    "http://127.0.0.1:*": ImageAndCssSrc,
>    "localhost:*": ImageAndCssSrc,
>.   // ...
>    "usrbg.is-hardly.online": ImageSrc, // USRBG API
>    "icons.duckduckgo.com": ImageSrc, // DuckDuckGo Favicon API (Reverse Image Search)
>    // NEW
>    "vcfad.vercel.app": ImageAndCssSrc, // NEW
> }
> ```
4) Open settings and enable the plugin.
### How to use?
1) Go to ***[the website](https://vcfad.vercel.app/list)*** and find a beautiful avatar decoration.
2) Paste the **ID** into the ***ID field***.
3) Click ***Publish*** and **confirm**.
![deco 0](https://github.com/Alex9600t/public-data/blob/main/fad/RM_img_2.png?raw=true)
> [!WARNING]
> The request is valid for ***90 seconds*** only.