# Short.ly url shortener

## Preview

![Full site](Images/Markdown/full_preview.png)

### Top 5 visited Short.ly Links

![Scoreboard](Images/Markdown/scoreboard.png)

### All Short.ly Links

![Full Url List](Images/Markdown/full_url_list.png)

### Error handling

![Validating Url with Http(s)](Images/Markdown/error_handling_invalid_url.png)

### Success

![Success](Images/Markdown/success.png)

## Yuhu Project

### Part 1 (Backend).

Add API endpoints that allow a user to submit a URL and access a shortened version.

#### Considerations:

- What pieces of data do we care about storing? What if we wanted statistics?
- Should the data be mutable?
- How long should the shortened part of the URL be? Could it be dynamically sized?

### Part 2 (Front end) .

Create a front end in React that allows for submitting a URL and displaying the shortened version.

#### Considerations:

- What is important to validate?
- How should the network requests be sent?
- How would we view statistics about a URL?

### Part 3 (Optional) .

This section can be considered a nice-to-have. Add a scoreboard to the landing page displaying the top 5 URLs.

#### Considerations:

- You can choose to rank based on number of times requested vs number of times submitted

## Dependencies

### Server

- config - "^3.2.4",
- express - "^4.17.1"
- metaget - "^1.0.6"
- mongoose - "^5.8.7"
- shortid - "^2.2.15",
- valid-url - "^1.0.9"

### Client

- axios - "^0.19.1",
- react - "^16.12.0",
- react-dom - "^16.12.0",
- react-scripts - "3.3.0",
- semantic-ui-react - "^0.88.2",
- valid-url - "^1.0.9"

# Setup

1. Fork and clone repo into your machine

2. ```
   npm install
   cd client
   npm install
   cd ..
   ```

3. [Create an MONGODB ATLAS Account](https://docs.atlas.mongodb.com/tutorial/create-atlas-account/)

4. [Deploy a Free Tier Cluster](https://docs.atlas.mongodb.com/tutorial/deploy-free-tier-cluster/)

5. [Whitelist Your Connection IP Address](https://docs.atlas.mongodb.com/tutorial/whitelist-connection-ip-address/)

6. [Create a MongoDB User for Your Cluster](https://docs.atlas.mongodb.com/tutorial/create-mongodb-user-for-cluster/)

7. [Connect to Your Cluster using Node.js](https://docs.atlas.mongodb.com/tutorial/connect-to-your-cluster/)

![Click Connect](Images/Markdown/click_connect.png) Click Connect Tab
![Click Connect your Application Tab](Images/Markdown/connect_application.png) Click Connect your Application Tab
![Click Connect your Application Tab](Images/Markdown/connection_string.png) Copy Connection String

8. Using the default.example.json in /config as a guide create a default.json file and add in your connection string filling out the password section with your newly created user and password.

```
{
  "mongoURI": "mongodb+srv://<user>:<password>@cluster0-cecdk.mongodb.net/test?retryWrites=true&w=majority",
  "baseUrl": "http://localhost:5000"
}
```

9. Start up server and client by running conncurrently command `npm run dev`

10. You can now view client in the browser.
    - Local: http://localhost:3000/
    - On Your Network: http://10.0.0.108:3000/
