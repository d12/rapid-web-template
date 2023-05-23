# Cloudflare template

The beginnings of a new project template for spinning up projects quickly. Goals:

- Rapid deployment in <30 seconds
- $0 cost for new demos
- No manual devops work, projects can be bootstrapped on the commnd line.

## Stack

I'll be using Cloudflare as the primary provider for this template as it solves all of the above goals at low cost.

- I can point URLs to R2 buckets for rapid static asset deployment
- Cloudflare Workers allow for rapid backend deployment
- Cloudflare D1 offers lightweight DB integration
- The startup plan means I get all of ^ for free

## Work to be done:

- [ ] Cloudflare Workers in template
- [ ] Scripts to spin up a new project from the template
- [ ] Deployment scripts
- [ ] Guides for others who want to use this project
