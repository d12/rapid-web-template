# Cloudflare template

A project template for spinning up web projects quickly.

## Current state

This template is missing a lot of core web-app features. I'll add more as I develop more projects with it.

## Idealogy

- New ideas should be developed and validated rapidly
- Developing a fixed and simple foundation will allow me to spend less time on scaffolding
- Difficult-to-reverse commitments should be avoided when prototyping. E.g. domain naming.
- Demos should cost me $0 or close to it.
- Time-to-demo of <1 week should be possible with a solid foundation and template

## Stack

I'll be using Cloudflare as the primary provider for this template as it solves all of the above goals at low cost.

- I can point URLs to R2 buckets for rapid static asset deployment
- Cloudflare Workers allow for rapid backend deployment
- Cloudflare D1 offers lightweight DB integration
- The startup plan means I get all of ^ for free

I'm also using MUI as a frontend framework because it's what I know well and it'll let me iterate rapidly.

## Copying the template

```
./scripts/copy-template
Project name: demo2

Copying template to /Users/d12/dev/cloudflare-template/demo2...

Copying files...

Copying Gemfile/Gemfile.lock...

Setting project name in package.json...

Setting project name in config.json...

Setting permission bits on scripts...

Running bundle install...
Using aws-eventstream 1.2.0
Using aws-partitions 1.767.0
Using aws-sigv4 1.5.2
Using jmespath 1.6.2
Using aws-sdk-core 3.173.0
Using aws-sdk-kms 1.64.0
Using aws-sdk-s3 1.122.0
Using bundler 2.4.9
Using parallel 1.23.0
Using ruby-progressbar 1.13.0
Bundle complete! 3 Gemfile dependencies, 10 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.

Done!

Do you want to deploy? (Y/n)
y

Deploying...
Building frontend...
Done.
Uploading static assets to R2... |Time: 00:00:00 | ======================================================================================================= | Time: 00:00:00
Done.

 Deployed! You can visit https://dev.natw.io/demo2 to see your new project.

Done!
```

## Deploying the frontend

```
./scripts/deploy-fe

Deploying...
Building frontend...
Done.
Uploading static assets to R2... |Time: 00:00:00 | ======================================================================================================= | Time: 00:00:00
Done.
```

## Work to be done:

- [ ] Cloudflare Workers in template
- [ ] Guides for others who want to use this project
- [ ] Support rollbacks, warnings on overwrite, and other safeguards
- [ ] Clean up old JS bundles from bucket without downtime
