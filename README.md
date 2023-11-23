# Youtube-clone in ReactJS ⚛️

![Screenshot of the Application](https://github.com/Rancha124/youtube-clone/assets/116198388/4a531cfe-7add-4ede-8e9b-5bd98a546101)

## Table of content 📝
1. Features
2. Tech Stack
3. Getting Started
4. Understand Context Api
5. Contribute

## 1. Features 🎯

<details>
  <summary>1. Infinite Scrolling</summary>
  <ul>
    <li>Implemented infinite scrolling using the powerful <a href="https://www.npmjs.com/package/react-infinite-scroll-component">react-infinite-scroll-component</a> library.</li>
    <li>Experience the same seamless scrolling used by platforms like Facebook, Instagram, YouTube, and TikTok, etc.</li>
  </ul>
</details>

<details>
  <summary>2. Modern Dark Theme</summary>
  <ul>
    <li>Most modern applications use a dark theme.</li>
    <li>It's an eye-comfortable and highly demanded feature.</li>
  </ul>
</details>

<details>
  <summary>3. Loading UI</summary>
  <ul>
    <li>I have used the Chakra UI <a href="https://chakra-ui.com/docs/components/skeleton">Skeleton</a> component for loading.</li>
    <li>It's a very important feature for a good user experience.</li>
  </ul>
</details>

<details>
  <summary>4. Country Option 🌍</summary>
  <ul>
    <li>I have provided users with a country option to filter videos.</li>
    <li>With this option, users can embark on a journey around the world and become creative thinkers.</li>
  </ul>
</details>

<details>
  <summary>5. Autocomplete Search Bar</summary>
  <ul>
    <li>I created an Autocomplete Search bar using the Google Queries API - <em>https://suggestqueries.google.com/complete/search?client=youtube&ds=yt&num=10&q=${query}</em></li>
    <li>The Autocomplete Search bar provides a similar experience to YouTube for my application.</li>
  </ul>
</details>

<details>
  <summary>6. Mobile Responsive</summary>
  <ul>
    <li>This application is designed to be mobile-friendly, ensuring that users can enjoy its features on various devices.</li>
  </ul>
</details>


## 2. Tech Stack
1. ⚛️ **[ReactJS](https://react.dev/)** - A popular JavaScript library for building user interfaces, known for its component-based architecture and efficient rendering.
2. 💎 **[Chakra UI](https://chakra-ui.com)** - A flexible and accessible UI component library for React that makes it easy to create visually appealing and responsive user interfaces.
3. Packages
   - [react-router-dom](https://reactrouter.com/web/guides/quick-start)
   - [react-icons](https://react-icons.github.io/react-icons/)
   - [react-infinite-scroll-component](https://www.npmjs.com/package/react-infinite-scroll-component)
   - [axios](https://axios-http.com/docs/intro)
   - [react-youtube](https://www.npmjs.com/package/react-youtube)
   - [framer-motion](https://www.framer.com/api/motion/)
   - [lodash](https://lodash.com/docs/)
   - [date-fns](https://date-fns.org/)
   - [numeral](https://numeraljs.com/)


## 3. Getting Started ▶️

Follow these steps to set up and run the project on your local machine.

#### 1. Clone the Repository

To get a local copy of this repository, run the following command in your terminal:

```sh
git clone https://github.com/Rancha124/youtube-clone.git
```

#### 2. Navigate to the Project

Change your working directory to the project folder:

```sh
cd youtube-clone
```

#### 3. Install Dependencies

Install the required packages using npm:

```sh
npm i
```
#### 4. API KEY Setup

To fetch YouTube data, you'll need the following `API_KEYS`. Follow these steps to set them up:

1. Obtain a **YouTube API key from Google** by visiting [Google Developers - Getting Started](https://developers.google.com/youtube/v3/getting-started). If you need detailed instructions, you can also refer to [How to Get a YouTube API Key](https://blog.hubspot.com/website/how-to-get-youtube-api-key).
2. Get a YouTube V3 API key from [Rapid API - YouTube V3](https://rapidapi.com/ytdlfree/api/youtube-v31). If you haven't used Rapid API before, you'll need to sign up after signup subscribe to the **YouTube V3 API** for free.

Once you have your API keys, proceed with the following:

3. Create a `.env` file in the `root` directory of your project.
4. Place your API key values in the `.env` file as shown below. 

```sh
REACT_APP_YOUTUBE_API_KEY_GOOGLE=YOUR_API_KEY
REACT_APP_YOUTUBE_API_KEY_RAPIDAPI=YOUR_API_KEY
```

> Note :- The `REACT_APP` prefix is used to define environment variables in a React application. These variables are used during the build process and can be accessed in your code using `process.env.REACT_APP_VARIABLE_NAME`.


#### 5. Start the Project

Run the following command to launch the ReactJS project in your local environment:

```sh
npm start
```

#### 6. Access the Project

Open your web browser and go to [http://localhost:3000](http://localhost:3000) to view the project.

That's it! Happy coding! 🚀


## 4. Understand Context API 🧠 

`YoutubeContext.js` module is created to streamline the handling of YouTube data within your React application. It utilizes React's Context API to establish a centralized state and methods, making it easier to manage and fetch YouTube-related information.

Key Features:

- Retrieve popular videos based on the country code.
- Provide auto-complete suggestions for search queries.
- Get search results for user-entered video queries.
- Manage API calls and loading states efficiently.
- To support mobile screen compatibility lacking in the initial API, 
I've integrated a secondary API for generating autocomplete suggestions. Although the first API has unlimited access on desktop, I opted to utilize both due to these differences.
- In functions such as getSearchVideos and getTrendingVideo, I've integrated the second API as a backup. This setup ensures uninterrupted service by seamlessly shifting to the second API when the first one reaches its usage limit. This strategy boosts application reliability and offers users a smoother experience.