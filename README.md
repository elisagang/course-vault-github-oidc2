<header>

<!--
  <<< Author notes: Header of the course >>>
  Read <https://skills.github.com/quickstart> for more information about how to build courses using this template.
  Include a 1280×640 image, course name in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Next to "About", add description & tags; disable releases, packages, & environments.
  Add your open source license, GitHub uses Creative Commons Attribution 4.0 International.
-->

# Getting secrets from HashiCorp Vault with GitHub OIDC in Action workflows

Understand the principles behind configuring OIDC authentication from GitHub Action workflows to HashiCorp Vault for least-privilege access to secrets from CI/CD pipelines.

</header>

<!--
  <<< Author notes: Finish >>>
  Review what we learned, ask for feedback, provide next steps.
-->

## Finish

_Congratulations friend, you've completed this course! :1st_place_medal:_

Here's a recap of all the tasks you've accomplished in your repository:
- Configure Vault to accept GitHub OIDC authentication requests
- Customize the `bound_claims` of a Vault role to provide fine-grained access control across workflows
- Create a workflow that can only retrieve secrets when triggered by a pull request
- Create a workflow that can only retrieve secrets when triggered by a push to the `main` branch
- Create jobs in a workflow that can only retrieve secrets when assigned to a specific GitHub Environment, and can't access each other's secrets

Remember that configuring Vault roles should typically happen separately from consuming secrets, so you'll likely want to create a separate workflow that creates Vault roles.
However, for the sake of this course, we've configured Vault roles in the same workflows that consumed secrets.

### What's next?

- We'd love to hear what you thought of this course [in our discussion board](https://github.com/artis3n/course-vault-github-oidc/discussions).
- You can combine multiple claims in a single Vault role to provide even more fine-grained access control!
For example, learn how to combine `sub` and `job_workflow_ref` to [provide secrets for reusable workflows](https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/using-openid-connect-with-reusable-workflows).
- Read [this comprehensive article](https://www.digitalocean.com/blog/fine-grained-rbac-for-github-action-workflows-hashicorp-vault) to learn how DigitalOcean employs this GitHub OIDC pattern for streamlined secrets management.
- Use this [Terraform module](https://github.com/digitalocean/terraform-vault-github-oidc) from DigitalOcean to help manage your GitHub OIDC Vault role configurations.

<footer>

<!--
  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---

Get help: [Post in our discussion board](https://github.com/artis3n/course-vault-github-oidc/discussions) &bull; Something not working? [File an issue ticket](https://github.com/artis3n/course-vault-github-oidc/issues)

&copy; 2022 Ari Kalfus &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [CC-BY-4.0 License](https://creativecommons.org/licenses/by/4.0/legalcode)

</footer>
