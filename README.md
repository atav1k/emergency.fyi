## Getting started

### Running the project

However you get the code, you can install dependencies and run the project in development mode with:

```bash
cd emergency.fyi
npm install # or yarn
npm run dev
```

Open up [localhost:3000](http://localhost:3000) and start clicking around.

Consult [sapper.svelte.dev](https://sapper.svelte.dev) for help getting started.


## Structure

Sapper expects to find two directories in the root of your project —  `src` and `static`.


### src

The [src](src) directory contains the entry points for your app — `client.js`, `server.js` and (optionally) a `service-worker.js` — along with a `template.html` file and a `routes` directory.

## Updating Case Data

Download the latest cases from the new york times data source:
> `curl https://raw.githubusercontent.com/nytimes/covid-19-data/master/us-counties.csv > cases-by-date-and-county.csv `

Group the cases by county and state and dump them as a massive JSON file so we can generate static pages and components for them:

> `node group-cases-by-county.js > data-by-counties.json`