
### How To Use

Yes, you can fork this repo. Please give me proper credit by linking back to [anaflous.com](https://anaflous.com). Thanks!

## 🛠 Installation & Set Up

1. Clone the repo CLI

   ```sh
   git clone https://github.com/hktitof/my-website.git
   ```

2. Install and use the correct version of Node using [NVM](https://github.com/nvm-sh/nvm)

   ```sh
   nvm install
   ```

3. Install dependencies

   ```sh
   yarn
   ```
   
4. (OPTIONAL) : Add .env file to the root project 
 
```bash
    touch .env
```

5.  (OPTIONAL) : Add your Google API key inside .env file.

###### ***Note :***
###### not Adding Google API to the project will cause not returning the correct zip code, it might be always "00000"
###### make sure you enabled Geolocation to this API

```Javascript
    NEXT_PUBLIC_KEY_GOOGLE_API="your API key"
```

6. Start the development server

   ```sh
   yarn dev
   ```

## 🚀 Building and Running for Production

1. Generate a full static production build

   ```sh
   yarn build
   ```

1. Preview the site as it will appear once deployed

   ```sh
   yarn run serve
   ```
---
## API Description :
##### Endpoint 1 :
the following endpoint will return a json object contains a bunch of information about the ip address  

```api
    /api/userInfoByIP/[IP-Address]
```
example :

```api
    /api/userInfoByIP/159.89.173.104
```
###### ***Get Request to above endpoint will return the following json data :***
```JavaScript
    {"zip":"560002","country":"India","countryCode":"IN","region":"KA","regionName":"Karnataka","city":"Bengaluru","datetime":"9/6/2022, 1:24:30 AM","lat":12.9634,"lon":77.5855,"timezone":"Asia/Kolkata","isp":"DigitalOcean, LLC","org":"Digital Ocean","as":"AS14061 DigitalOcean, LLC","query":"159.89.173.104"}
```

##### Endpoint 2 :
the following endpoint will return a json object contains the zip code for the latitude and logitude

```api
    "/api/userInfoByLatLon/" + lat + "/" + lon
```
example :

```api
    /api/userInfoByIP/159.89.173.104
```
###### ***Get Request to above endpoint will return the zipcode of the lat and long provided :***
```JavaScript
    {"zipcode" : "56998"}
```
###### ***the Response below is returned if the lat and long provided has no zip code in Google maps, like lat & long in positioned in the ocean :***
```JavaScript
    {"zipcode" : "00000"}
```

##### Endpoint 3 :
the following endpoint will return a json object contains "quote" and "author", for SpeedTyping project i displayed only the quote, **minLength** is considered as the minimum of characters.  

```api
    /api/typing/[minLength]
```
##### notes : 
- ***minLength*** should be between 10 - 300.
- the returned quote is a chain of 
- i costumized the original Endpoint using The API Route of Nextjs, here is the Original Endpoint.

##### Original Endpiont :
###### URL : 
```api
    https://api.quotable.io/random?minLength=[minLength]
```
---

## References

| Color          | Hex                                                                |
| -------------- | ------------------------------------------------------------------ |
| Navy           | ![#0a192f](https://via.placeholder.com/10/0a192f?text=+) `#0a192f` |
| Light Navy     | ![#112240](https://via.placeholder.com/10/0a192f?text=+) `#112240` |
| Lightest Navy  | ![#233554](https://via.placeholder.com/10/303C55?text=+) `#233554` |
| Slate          | ![#8892b0](https://via.placeholder.com/10/8892b0?text=+) `#8892b0` |
| Light Slate    | ![#a8b2d1](https://via.placeholder.com/10/a8b2d1?text=+) `#a8b2d1` |
| Lightest Slate | ![#ccd6f6](https://via.placeholder.com/10/ccd6f6?text=+) `#ccd6f6` |
| White          | ![#e6f1ff](https://via.placeholder.com/10/e6f1ff?text=+) `#e6f1ff` |
| Green          | ![#64ffda](https://via.placeholder.com/10/64ffda?text=+) `#64ffda` |

---

---
# sifunadonnex
