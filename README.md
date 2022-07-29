# Frontity - Vercel builder

Use this builder to deploy a [Frontity](https://frontity.org) project in the Vercel. This package is a fork of [@frontity/now](https://www.npmjs.com/package/@frontity/now)

## Before deploying

1. Create this `vercel.json` file in your project and change the site url:

```json
{
	"version": 2,
	"builds": [
		{
			"src": "package.json",
			"use": "@whale-agency/vercel"
		}
	]
}
```

2. Create an account on Vercel. You can [signup here](https://vercel.com/signup).

3. Log in the terminal:

```bash
> npx vercel login
```

## Deploy a test site

Deploy Frontity using this command:

```bash
> npx vercel
```

That will give you a unique URL for that deploy. Check that everything is ok.

## Deploy a production site

You need to [add a CNAME](https://vercel.com/docs/concepts/projects/custom-domains#option-2:-using-external-nameservers) of `www.your-site.com` to `cname.vercel-dns.com` in your domain DNS settings.

Then, deploy Frontity using this command:

```bash
> npx vercel --prod
```

That will create a deploy and assign it to your real site url.
