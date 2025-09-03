Terraform Provider GitHub
=========================

<img src="https://cloud.githubusercontent.com/assets/98681/24211275/c4ebd04e-0ee8-11e7-8606-061d656a42df.png" width="72" height="">

<img src="https://raw.githubusercontent.com/hashicorp/terraform-website/d841a1e5fca574416b5ca24306f85a0f4f41b36d/content/source/assets/images/logo-terraform-main.svg" width="300px">

This project is used to manipulate GitHub resources (repositories, teams, files, etc.) using Terraform. Its Terraform Registry page can be found [here](https://registry.terraform.io/providers/tf-providers/github/).

## About this fork

This repository is a community-maintained fork of the [official GitHub Terraform provider](https://github.com/integrations/terraform-provider-github/).
It is based on [integrations/github](https://github.com/integrations/terraform-provider-github/), with the goal of:
- Pulling in and releasing upstream contributions faster.
- Providing additional functionality without waiting for upstream release cycles.
- Staying as close to upstream as possible to minimize drift.

> [!NOTE]
> If upstream resumes regular releases and merges community PRs promptly, this fork may be deprecated in favor of the official provider.

## Migration from the official provider

When upgrading from `integrations/github` to `tf-providers/github`, run the following. Otherwise, Terraform will still require the old provider to interact with the state file.

```sh
terraform state replace-provider \
  integrations/github \
  tf-providers/github
```

## Requirements

-	[Terraform](https://www.terraform.io/downloads.html) 0.10.x
-	[Go](https://golang.org/doc/install) 1.19.x (to build the provider plugin)

## Usage

Detailed documentation for the GitHub provider can be found [here](https://registry.terraform.io/providers/tf-providers/github).

## Contributing

Do not open PRs against this repository.
- Please submit all new features and bug fixes to [upstream](https://github.com/integrations/terraform-provider-github/) so they can be merged into the official provider.
- If you want a change from upstream to be included here, open an issue in this repo requesting that the fork pull it in.

Our wish is for upstream to eventually contain all functionality avilable this this fork.

## Support

GitHub Support does not provide support for this integration. This is a community-supported project.
