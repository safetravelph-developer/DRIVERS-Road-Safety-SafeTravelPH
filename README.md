# DRIVERS-Road-Safety-SafeTravelPH

## Project Folder Structure

The project consists of four main folders:

- **`assets`** - This folder contains all icons and images used in the web application.
- **`components`** - This folder holds reusable UI components such as dialogs, navigation bars, menu items, headers, and report dialogs. Many of the key functionalities are implemented within these components.
- **`query and mutations`** - This folder contains all GraphQL queries and mutations used to fetch and manipulate data in the application.
- **`screens`** - This folder contains all the pages of the web application, including forms, maps, tables, and other user interface screens.

## Important Pages

### Map (`/screens/map.js`)

This page displays all incident data, including a heatmap view. Users can filter incidents by child-related incidents or view all incident data. There is also an option to add a new report by clicking the 'Add Report' button after the filter button in the navigation bar. When clicked, users can select a location on the map, which triggers a dialog where they can input incident report details.

### List (`/screens/list.js`)

This page lists all incidents in a table format. Users can click on a row (date and time) to view full incident details. Sorting and filtering options are also available.

### Reports (`/screens/reports.js`)

This page lists all incident reports. Users can filter reports based on their needs and also sort and filter the table.

### Charts (`/screens/charts.js`)

This page displays incident reports as charts, categorized by year. The GraphQL query can be edited to retrieve specific data based on user needs. This page is still under development and may receive further enhancements.

### Data Review (`/screens/stph.js`)

This page is designed for admins to validate all reports before they are added to the database. Users can review full report details and approve incidents before storing them permanently. This page also lists newly added reports pending validation.

## Setup Instructions

Before starting the project, you need to install the required dependencies and configure the environment variables.

### 1. Install Dependencies

Run the following command to install necessary modules and react-scripts:

```sh
npm install react-scripts --save --legacy-peer-deps
```

### 2. Configure Environment Variables

Edit the `.env.production` and `.env.development` files to include your own credentials:

#### `.env.production`

```sh
BROWSER=none

REACT_APP_DRIVER_API_URL=PROD_STATIC_GRAPHQL_URL
REACT_APP_GOOGLE_API_KEY=PROD_STATIC_GOOGLE_MAPS_API_KEY
REACT_APP_GOOGLE_CLIENT_ID=PROD_STATIC_GOOGLE_CLIENT_ID

REACT_APP_ACCOUNT_1_USERNAME=STATIC_ACCOUNT_1
REACT_APP_ACCOUNT_1_PASSWORD=STATIC_ACCOUNT_1

REACT_APP_ACCOUNT_2_USERNAME=STATIC_ACCOUNT_2
REACT_APP_ACCOUNT_2_PASSWORD=STATIC_ACCOUNT_2

REACT_APP_ACCOUNT_3_USERNAME=STATIC_ACCOUNT_3
REACT_APP_ACCOUNT_3_PASSWORD=STATIC_ACCOUNT_3

REACT_APP_ACCOUNT_4_USERNAME=STATIC_ACCOUNT_4
REACT_APP_ACCOUNT_4_PASSWORD=STATIC_ACCOUNT_4

REACT_APP_ACCOUNT_5_USERNAME=STATIC_ACCOUNT_5
REACT_APP_ACCOUNT_5_PASSWORD=STATIC_ACCOUNT_5
```

#### `.env.development`

```sh
BROWSER=none

REACT_APP_DRIVER_API_URL=DEV_STATIC_GRAPHQL_URL
REACT_APP_GOOGLE_API_KEY=DEV_STATIC_GOOGLE_MAPS_API_KEY
REACT_APP_GOOGLE_CLIENT_ID=DEV_STATIC_GOOGLE_CLIENT_ID

REACT_APP_ACCOUNT_1_USERNAME=STATIC_ACCOUNT_1
REACT_APP_ACCOUNT_1_PASSWORD=STATIC_ACCOUNT_1

REACT_APP_ACCOUNT_2_USERNAME=STATIC_ACCOUNT_2
REACT_APP_ACCOUNT_2_PASSWORD=STATIC_ACCOUNT_2

REACT_APP_ACCOUNT_3_USERNAME=STATIC_ACCOUNT_3
REACT_APP_ACCOUNT_3_PASSWORD=STATIC_ACCOUNT_3

REACT_APP_ACCOUNT_4_USERNAME=STATIC_ACCOUNT_4
REACT_APP_ACCOUNT_4_PASSWORD=STATIC_ACCOUNT_4

REACT_APP_ACCOUNT_5_USERNAME=STATIC_ACCOUNT_5
REACT_APP_ACCOUNT_5_PASSWORD=STATIC_ACCOUNT_5
```

You can edit these environment files to change the account usernames and passwords that can be used for logging in. To use different credentials, update `REACT_APP_ACCOUNT_1_USERNAME` and `REACT_APP_ACCOUNT_1_PASSWORD` (and so on up to Account 5) with your desired values.

Make sure to replace `PROD_STATIC_GRAPHQL_URL`, `DEV_STATIC_GRAPHQL_URL`, `PROD_STATIC_GOOGLE_MAPS_API_KEY`, `DEV_STATIC_GOOGLE_MAPS_API_KEY`, `PROD_STATIC_GOOGLE_CLIENT_ID`, and `DEV_STATIC_GOOGLE_CLIENT_ID` with your actual values.

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in development mode. Open [http://localhost:3000](http://localhost:3000) in your browser.

- The page reloads when you make changes.
- You may see lint errors in the console.

### `npm test`

Launches the test runner in interactive watch mode.
See more about [running tests](https://facebook.github.io/create-react-app/docs/running-tests).

### `npm run build`

Builds the app for production in the `build` folder.

- React is bundled in production mode and optimized for performance.
- The build is minified, and filenames include hashes.
- Your app is now ready for deployment!

### Deployment

For deployment instructions, check the official guide:
[Deployment Guide](https://facebook.github.io/create-react-app/docs/deployment)

### Troubleshooting

If `npm run build` fails to minify, check the troubleshooting guide:
[Troubleshooting Build Issues](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)

