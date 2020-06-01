## React application: "Search City Restaurants:
https://murmuring-island-72596.herokuapp.com/

#### '    1. How long did you spend on the coding test? What would you add to your solution if you had more time? If you didn't spend much time on the coding test then use this as an opportunity to explain what you would add.'
I spent around 10 hours overall: <br />
- Main functionality and test workflow - 5 hr. 
- ... from which debugging 2hr
- Responsive layout - 1hr 
- Accessibility - 1hr. 
- Heroku build dependencies and errors - 2hr 
- Git posting and Readme answers - 1hr 

If more time: 
- will add integration test and api tests (in addition to three standard template based test we have)
- will use Typescript to avoid type and undefined errors
- will use decomposition in small pure components
- will do real SEO
- will check accessibility using JAWS - a real Tool for visually impaired users
<br />

To suggest what to add? may be to offer a standard `package.json` so we will not think that a specific tool is prohibited, or we are limited only to Functional Style etc.<br />
Having specific versions fixed (may be close to those in production) will level up the environment for all applicants. 

### '    2. What was the most useful feature that was added to the latest version of your chosen language? Please include a snippet of code that shows how you've used it.'
Of course using Hooks on react functional components:<br />
`import React, {useState, useEffect} from 'react';`<br />
`import {useDispatch} from "react-redux";`<br />
` import axios from "axios";`<br />
`import {saveCity, refineCity} from "../../aredux";`
`import {HookCityContainer} from "../hooks/HookCityContainer";`<br />
 
 
 `export const DataCityFetchRefine = () => {`
 
     const dispatch = useDispatch()
     const itemsPerPagerPage = process.env.REACT_APP_ITEMS_PER_PAGER_PAGE
     const [post, setPost] = useState([])
     const [id, setId] = useState('')
     const [idFromButtonClick, setIdFromButtonClick] = useState('')
     const [err, setErrMsg] = useState(false)
     const [currPagerPage, setCurrPagerPage] = useState(1)
     const [totalEntries, setTotalEntries] = useState(0)
     const [currCity, setCurrentCity] = useState('')
     const [postError, setPostError] = useState({})
     const [refine, setRefine] = useState('')
     const [refineValue, setRefineValue] = useState('')`
### '    3. How would you track down a performance issue in production? Have you ever had to do this?'
Chrome Performance tab routinely is used during development and for production performance testing.
I would run a load test on the api call to find out how many concurrent calls can it handle from time to time. 
Log the results and identify the bottleneck.<br />
React DevTools and Redux Dev Tools extension are the everyday tool during development to find bottlenecks.

### '    4. How would you improve the API that you just used?'
currently this api only returns restaurant list based on one parameter which is city. 
The task also indicates that some:
- info is needed `Cuisine Types and Rating of the restaurant` shall be shown. But that info is not part of the API
- also `Area` field is not informative - it does not change with in City so using it in `Refine` field is not productive.
### '    5. Please describe yourself using JSON.'
Use it in backend (`Node js/Express`, `PHP`) as well as frontend (`React`, `Jsavascript`, `PHP`) <br />
Always feel a relief when see `JSON` answer in the request - now we may continue with other functionality as the data is already OK.
<br />
Having JSON at the base of `NoSQL document model` like `MongoDb` easy development for programmers already comfortable wit JSON format in general.
