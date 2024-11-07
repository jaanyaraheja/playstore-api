# Unofficial PlayStore API

**Explore android app metadata from PlayStore with ease!**

[![Build & Deploy](https://github.com/rajkumaar23/api-playstore/actions/workflows/deploy.yaml/badge.svg)](https://github.com/rajkumaar23/api-playstore/actions/workflows/deploy.yaml)
[![Nightly Test](https://github.com/rajkumaar23/api-playstore/actions/workflows/test.yaml/badge.svg)](https://github.com/rajkumaar23/api-playstore/actions/workflows/test.yaml)

## Usage

Retrieve comprehensive JSON data for any app from Google Play by making a simple GET request:
```
https://api-playstore.rajkumaar.co.in/json?id=<YOUR-PACKAGE-ID>
```
Example : https://api-playstore.rajkumaar.co.in/json?id=com.dd.doordash

Sample JSON response with all possible details:
```json
{
    "packageID": "com.dd.doordash",
    "name": "DoorDash - Food Delivery",
    "version": "15.156.24",
    "downloads": "50,000,000+",
    "downloadsExact": 61535856,
    "lastUpdated": "Mar 29, 2024",
    "launchDate": "Mar 26, 2015",
    "developer": "DoorDash",
    "screenshots": [
        "https://play-lh.googleusercontent.com/b-ZRIvKPErodCjPJo47AB_Fl1dGgOUAGoe03OjER7lzZPffz3Cv0xgMniNHfRYR-bQg",
        "https://play-lh.googleusercontent.com/-z9S93iM5RR6xOU8Sj774aNZsSATCZymn3fJiOnzW1VuGteh5vLfgyTjIiKOMhCFfjc",
        "https://play-lh.googleusercontent.com/2iNMFwIwCHD8otkfT_AgZU62UNqJziCay3uEVEDFrXmz78wuOf-hTNZbLwdEgShWcfM",
        "https://play-lh.googleusercontent.com/UZPWjpQcp-3U2FeUxAIuU9zX2P-z4rhKwmH0hyyr4sUQoKVUotKb_SdhuRBxMW0KsuY",
        "https://play-lh.googleusercontent.com/jUcGpu7azj7RwB4brZyq1xoCzyobyUkHwyNcuhfZJK-6DDvm7AFB0ldsTP4Hs2h5UsHg",
        "https://play-lh.googleusercontent.com/3Fkc_6o-818jRxVuP42rluJNjx_CQ77Bs8Fx-HDD6jAxRmD-irJLsMAtiIvm3sC8qeZN"
    ],
    "category": "Food \u0026 Drink",
    "logo": "https://play-lh.googleusercontent.com/Fvled-zLfL8ER0EBNIk-FnunJCcH2u_T6rdITclOFdU2jpEopdMstZOHP-PtuhP_5coZ",
    "banner": "https://play-lh.googleusercontent.com/TmWukTjL87iibmuHXhc9d04Hvul6nErQXE0nRcJvvsiFffDBjE0JmGns57r1x1RihMA",
    "privacyPolicy": "https://www.doordash.com/privacy/",
    "latestUpdateMessage": "Our mission is to deliver good by connecting people and possibility. If we can play a small role in helping you spend more time with your friends and family or get ahead on your favorite projects, then we have delivered good.\u003cbr\u003e\u003cbr\u003eWe’re launching a new set of initiatives to deliver good within our communities, and you’ll see a new visual identity that reflects our spirit. Thank you for making DoorDash a success — we wouldn’t be here without you.\u003cbr\u003e\u003cbr\u003eUpward and onward!\u003cbr\u003eTony Xu, CEO and Co-Founder",
    "website": "https://www.doordash.com/",
    "supportEmail": "support@doordash.com",
    "rating": "4.6",
    "noOfUsersRated": "4,299,422",
    "description": "Delivery anywhere you are. DoorDash offers the greatest online selection of your favorite restaurants and stores, facilitating delivery of freshly prepared meals, groceries, OTC medicines, flowers \u0026amp; more...",
}
```

## Integration with [Shields.io](https://shields.io)
Customize your README with dynamic badges for specific attributes. Utilize the following template:
```markdown
![Badge](https://img.shields.io/endpoint?url=https://api-playstore.rajkumaar.co.in/<ATTRIBUTE-NAME>?id=<PACKAGE-ID>)
```
Supported attributes: 
- packageID
- name
- version
- downloads
- downloadsExact
- lastUpdated
- launchDate
- developer
- description
- screenshots
- category
- logo
- banner
- privacyPolicy
- latestUpdateMessage
- website
- supportEmail
- rating
- noOfUsersRated

Explore customization options based on shields.io style parameters. Learn more [here](https://shields.io/).

### Examples

Downloads
```markdown
![Downloads Badge](https://img.shields.io/endpoint?color=success&url=https://api-playstore.rajkumaar.co.in/downloads?id=com.dd.doordash)
```
![Downloads Badge](https://img.shields.io/endpoint?color=success&url=https://api-playstore.rajkumaar.co.in/downloads?id=com.dd.doordash)

Version
```markdown
![Version Badge](https://img.shields.io/endpoint?color=blue&url=https://api-playstore.rajkumaar.co.in/version?id=com.dd.doordash)
```
![Version Badge](https://img.shields.io/endpoint?color=blue&url=https://api-playstore.rajkumaar.co.in/version?id=com.dd.doordash)

Developer
```markdown
![Dev Badge](https://img.shields.io/endpoint?color=orange&style=for-the-badge&url=https://api-playstore.rajkumaar.co.in/developer?id=com.dd.doordash)
```
![Dev Badge](https://img.shields.io/endpoint?color=orange&style=for-the-badge&url=https://api-playstore.rajkumaar.co.in/developer?id=com.dd.doordash)

### Known Issues

- The API may respond with a **0** for `rating`/`noOfUsersRated` because the ratings on Google Play Store are specific to a country/region and the API is only able to fetch ratings that are local to the United States.

### License
Find the license [here](LICENSE)


