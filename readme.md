# New project

To start a project create a folder, you in to folder, there command npm init, you follow the steps.

Install express, command npm i express

Create file index.js and typped:
```
const express = require('express')
const app = express()

app.get('/', (req, res) => {
    res.json({ mensaje: 'Hola mundo' })
})

app.listen(3000, () => {
    console.log('http://localhost:3000')
})
```

# Vercel

To deploy in vercel you must add file vercel.json

```
{ 
    "version": 2, 
    "builds": [
        {
            "src":"index.js",
            "use": "@vercel/node"
        }
    ],
    "rewrites": [{ "source": "/(.*)", "destination": "/" }] 
}
```
The app must storage in github, vercel will ask you for your repository in github

Where index.js is your file to init app

Add enviroment varibles in deployment in platform vercel 

Reference
https://www.youtube.com/watch?v=iz2wBaKStNM

Este se subira a vercel