**Welcome to UK Delivers.**

UK Delivers is a simple directory of independent businesses offering local delivery. Enabling people to stay at home and save lives, while keeping our high streets alive.

This project was originally bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

_Credit Rob Hough._

For reference, there are currently three versions available on GitHub:

* Deal Delivers: [https://github.com/heymynameisrob/deal-delivers-app](https://github.com/heymynameisrob/deal-delivers-app)
* Dulwich Delivers: [https://github.com/tomszekeres/dulwich-delivers-app](https://github.com/tomszekeres/dulwich-delivers-app)
* Reigate Delivers: [https://github.com/robin174/reigate-delivers-app](https://github.com/robin174/reigate-delivers-app)

# Accounts required

There are four accounts required to get a UK Delivers app online.

* [Airtable](https://airtable.com) - For your database and listing form
* [Netlify](https://www.netlify.com) - For deployment
* [MailChimp](https://mailchimp.com) - For email sign-ups
* [Cloudinary](https://cloudinary.com) - For hosting images on a Content Delivery Network (CDN)

A domain is also required. We recommend a '.com' URL for this.

# Brand

The design of each individual site is up to the owner and you will need to pick two hexadecimal values for your site; one for the large triangle and one for the smaller triangle. The base background blue is #0B132B.

_For reference, Reigate Delivers: Pink #E20C5E, Yellow #FFB600._

## Artwork generation

For help with generating the necessary artwork files - please email [robin@reigatedelivers.com](mailto:robin@reigatedelivers.com).

___

# Stage 01 - Local

**To start, let's get a base version of the site live locally.**

## Download template
Navigate to your local folder.Download and initialize git, or clone the repository. 

To get started you will need [Node.js](https://nodejs.org). You have a choice of package managers: [Node package manager (npm)](https://nodejs.org) or [Yarn](https://yarnpkg.com).

Using the terminal, navigate to your app folder.

##### Via npm
`npm install` to install the necessary Node modules. 

`npm start` to start the server, available at `http://localhost:3000/`.

**OR**

##### Via Yarn
`yarn install` to install the necessary Node modules

`yarn start` to start the server, available at `http://localhost:3000/`.

***NB. I had to update my version of Node.js - to update on Mac/Catalina:***

`nvm install node`

Once installation is complete, launch the app locally via:

`npm start` or `yarn start`

A local version of your site shoudl be available: 

`http://localhost:3000/`


### Customisation
Time to run through the files in the repo and update to your specific location. If you'd like to build on what we have created - go for it.


___

# Stage 02 - Online

**Once the app is available locally, let's get it online.**

## Upload template to GitHub
For the purposes of speed, we are currently working directly off `master`. Feel free to use a branch.

##### .gitignore
A `.gitignore` file should be included in your repo. If not, make sure you have one in place, otherwise `node_modules` will be uploaded to your repo.

To create a new file: 

`touch .gitignore`

And add `/node_modules` as your first entry. `Save`.

## Connect GitHub repo to Netlify
With a Netlify account created, let's get Netlify connected to your repository.

From Netify dashboard, visit `Sites` and click 'New site from `Git`.

Select your Git Provider: `GitHub`.

Connect to your respective GitHub account and select repository.

Select your `Owner` and `Branch to deploy` and define your `Basic build settings`. For me these are: 
 
* Build command: `yarn build`
* Publish directory: `build/`

Click `Deploy site`.

An initial `Site deploy` will start. Takes a minute or so to deploy. Once deployed, a Netlfiy subdomain will be generated. Visit the subdomain to verify all ok with the deployment.

You can revisit your deployments at any time from `Deploys` in the Netlify admin. 

## Connect Cloudinary to template
Cloudinary is currently the CDN we have in place to store the images used for each listing header.

Update Cloudinary credentials in `public` - `admin` - `config.yml`

***NB. I found that Cloudinary did not play nicely with Safari browser (The `insert` option did not appear).***

## Connect MailChimp to template

Update link to MailChimp list in `src` - `App.js`


Once live, please feel free to email [robin@reigatedelivers.com](mailto:robin@reigatedelivers.com) to let us all know your directory is live.










