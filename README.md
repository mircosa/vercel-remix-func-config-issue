# Repo to reproduce Vercel functions config issue with a Remix project

This is an blank Remix project with Vercel configured via the Remix CLI to reproduce the issue.

A vercel.json file was added to configure the function memory to 3008mb.

Upon building this project in Vercel the build will fail with the following message:

`Error: The pattern "api/index.js" defined in `functions` doesn't match any Serverless Functions inside the `api` directory.`



Open up [http://localhost:3000](http://localhost:3000) and you should be ready to go!


The vercel.json file contains.

`
{
  "functions": {
    "api/index.js": {
      "memory": 3008,
      "maxDuration": 60
    }
  }
}
`
