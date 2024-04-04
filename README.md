<p align="center">
<p align="center">
<img width="100%" src="./public/github_readme.jpg"/>

<center>

[Get started](https://revert.dev) · [Docs](https://docs.revert.dev/) · [Issues](https://github.com/revertinc/revert/issues) · [Discord](https://discord.gg/q5K5cRhymW) · [Get in touch](mailto:team@revert.dev)

</center>

<center>

[English](README.md) | [中国人](./translations/chinese/README.md) | [Deutsch](./translations/german/README.md) | [Português](./translations/portuguese/README.md)

</center>

[![Star us on GitHub](https://img.shields.io/github/stars/revertinc/revert?color=FFD700&label=Stars&logo=Github)](https://github.com/revertinc/revert)
![Vercel](https://therealsujitk-vercel-badge.vercel.app/?app=revert-client-git-main-revertdev) [![](https://dcbadge.vercel.app/api/server/q5K5cRhymW?style=flat)](https://discord.gg/q5K5cRhymW) [![twitter](https://img.shields.io/twitter/follow/Revertdotdev?style=social)](https://twitter.com/intent/follow?screen_name=RevertdotDev) ![Revert API](https://cronitor.io/badges/HnK0d9/production/OR5NlgURLI1wAT148KU6ycCBSSk.svg) [![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://docs.revert.dev/) <a href="https://github.com/revertinc/revert/pulse"><img src="https://img.shields.io/github/commit-activity/m/revertinc/revert" alt="Commits-per-month"></a>
<a href="https://github.com/revertinc/revert/tree/main/LICENSE.txt" target="_blank">
<img src="https://img.shields.io/static/v1?label=license&message=AGPL-3.0&color=white" alt="License">
</a>

</p>

#### Hacker News

<a href="https://news.ycombinator.com/item?id=37995761">
  <img
    style="width: 250px; height: 54px;" width="250" height="54"
    alt="Featured on Hacker News"
    src="https://hackernews-badge.vercel.app/api?id=37995761"
  />
</a>
<a href="https://www.producthunt.com/posts/revert-3?utm_source=badge-top-post-topic-badge&utm_medium=badge&utm_souce=badge-revert&#0045;3" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/top-post-topic-badge.svg?post_id=425023&theme=light&period=weekly&topic_id=267" alt="Revert - Open&#0045;source&#0032;unified&#0032;API&#0032;to&#0032;build&#0032;product&#0032;integrations | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>
<a href="https://www.producthunt.com/posts/revert-3?utm_source=badge-top-post-badge&utm_medium=badge&utm_souce=badge-revert&#0045;3" target="_blank"><img src="https://api.producthunt.com/widgets/embed-image/v1/top-post-badge.svg?post_id=425023&theme=light&period=daily" alt="Revert - Open&#0045;source&#0032;unified&#0032;API&#0032;to&#0032;build&#0032;product&#0032;integrations | Product Hunt" style="width: 250px; height: 54px;" width="250" height="54" /></a>

### ⭐ About Revert

Revert makes it incredibly easy to build integrations with any third party API such as

-   Go-to-market tools like CRMs (Salesforce, Hubspot).
-   Communication tools (Slack, MS Teams)
-   Ticketing tools like (Jira, Asana)

> We believe an **open source unified API** enables us to cover the long tail of third party APIs while empowering engineers to customise the integration code we offer out of the box. This way engineers can use us over building everything from scratch.

### Why Revert?

You might want to check us out if

-   You are developer building a B2B product
-   You have a ton of integrations on your roadmap
-   Your focus is building your core product vs maintaining integration code
-   You want to move fast and not break things

[Sign up](https://revert.dev) for an account or read our docs [here](https://docs.revert.dev) !

### 🚀 What makes us faster and reliable.

-   **Seamless Integration**: Revert has pre-configured apps on all these platforms so you don't have to create them and deal with nuances on each platform.
-   **Graceful Failure Handling**: Ensures smooth handling of expired permissions by customers, preventing any service disruptions.
-   **Automatic OAuth Token Refresh**: OAuth tokens are automatically refreshed, ensuring continuous API functionality.
-   **API Retry Mechanism**: Revert automatically retries failed API calls, improving reliability and minimizing potential issues.
-   **SDKs for Popular Frameworks**: Ready-to-use SDKs available for React, Vue, and Angular, enabling quick and easy integration.
-   **Self-Hosted**: Provides the flexibility to self-host the integration solution, giving you full control over deployment and data.

## Quickstart

#### Revert Cloud

The easiest way to get started is to create a [Revert Cloud account](https://app.revert.dev/sign-up). The cloud version offers the same functionality as the self-hosted one.

If you want to self-host Revert though, you can do that today with docker-compose as instructed below.

#### Spinning up Revert with docker-compose

The easiest way to start with self-hosted Revert is to run it via docker-compose:

```shell
# Get the code
git clone --depth 1 https://github.com/revertinc/revert

# Copy the example env file
cd revert
cp .env.example .env
cp packages/backend/.env.example packages/backend/.env
cp packages/client/.env.example packages/client/.env
cp packages/js/.env.example packages/js/.env
cp packages/react/.env.example packages/react/.env
cp packages/vue/.env.example packages/vue/.env

# Ensure that clerk is setup in `client` and a user is created by following the instructions here: https://docs.revert.dev/overview/developer-guide/developer-guide#-revertdotdev-client

# Update these .env files with any of your own secrets if you'd like to.

# Then In the root directory run

# When running for the first time to seed the database. (RUN ONLY ONCE)
docker-compose run db-seed

# For subsequent runs
docker-compose up -d

```

The UI is now available at http://localhost:3000 and the backend is available at http://localhost:4001.

## Architecture

### Connection flow for your app's users with Revert

<img src="./public/connection_flow.png"/>

### Architecture Overview

<img src="https://res.cloudinary.com/dfcnic8wq/image/upload/v1697107526/Revert/how4gj3vp2wch4kw2akb.png" />

## Packages

This repo contains a set of packages under `@reverdotdev/` namespace such as:

-   [`@revertdotdev/backend`](./packages/backend): The core Revert API that powers the frontend SDKs.
-   [`@revertdotdev/revert-react`](./packages/react): Official SDK for React.
-   [`@revertdotdev/revert-vue`](./packages/vue): Official SDK for Vue.
-   [`@revertdotdev/js`](./packages/js): Official SDK for Javascript.
-   ...

## Examples

The repo [`revert-example-apps`](https://github.com/revertinc/revert-example-apps) contains a set of examples how to use revert with different frameworks.

## 📞 Support

In case of questions/feedback, you can get in touch in the following ways

-   Open a Github support issue
-   Contact us at [email](mailto:team@revert.dev)
-   Ask a question in our [discord](https://discord.gg/q5K5cRhymW)
-   If you'd like you can book a call with our team below

<a href="https://cal.com/jatinsandilya/chat-with-jatin-from-revert?utm_source=banner&utm_campaign=oss"><img alt="Book us with Cal.com" src="https://cal.com/book-with-cal-dark.svg" /></a>

## 🔒 Security

We take security seriously.

**Please do not file GitHub issues or post on our public forum for security vulnerabilities**.

Email `security@revert.dev` if you believe you have uncovered a vulnerability. In the message, try to provide a description of the issue and a way of reproducing it.

## 🗺️ Roadmap

CRMs:

-   [x] **Salesforce**
-   [x] **Hubspot**

-   [x] **Zoho CRM**

-   [x] **Pipedrive**

-   [x] **Close CRM**
-   [ ] Other CRMs such as Zendesk Sell, MS 365

Communication tools:

-   [x] Slack
-   [x] Discord
-   [ ] Microsoft Teams

Accounting software:

-   [ ] Xero
-   [ ] Quickbooks

...[and more](https://github.com/revertinc/revert/issues?q=is%3Aissue+is%3Aopen+label%3AIntegration)

-   [ ] Ability to self-host Revert inside your own cloud
-   [ ] SOC 2 (In Progress)

Feel free to create an issue if you'd like an integration we're missing [here](https://github.com/revertinc/revert)

## 💪 Contributors

Thankful to the community for making Revert better every day ❤️

<a href="https://github.com/revertinc/revert/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=revertinc/revert" />
</a>
