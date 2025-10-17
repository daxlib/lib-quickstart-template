# `lib-quickstart-template` - Quickstart Template

A ready-to-use template containing everything you need to start developing your own DAX Lib library.

## 🚀 Getting Started

### 1. Create a New Repository from this Template

- Click [![Use this template](https://img.shields.io/badge/Use%20this%20template-brightgreen?logo=github)](https://github.com/daxlib/lib-quickstart-template/generate) to create your new repository based on this template.
- Enter a repository name that reflects the name of the library you want to develop.

> [!TIP]
> Need to develop more libraries? Simply reuse this template and generate a new repository for each one.

### 2. Fork the DAX Lib repository

- If you already created a fork of the [DAX Lib](https://github.com/daxlib/daxlib) repository, you can skip this step.
- Click [![Fork](https://img.shields.io/badge/Fork-brightgreen?logo=github)](https://github.com/daxlib/daxlib/fork) to create a fork of the official [DAX Lib](https://github.com/daxlib/daxlib) repository
- Your fork will be created in your GitHub account

> [!NOTE]
> A fork is required to create a pull request from your repository to the official [DAX Lib](https://github.com/daxlib/daxlib) repository. We recommend keeping the fork name as `daxlib` to simplify configuration. If you choose a different name, make sure to update the `DAXLIBFORK_NAME` variable in the workflow file `.github/workflows/publish-package.yml`.

## ⚙️ Repository Setup

Follow these steps to configure your new repository:

### 1. Create a Personal Access Token (PAT)

- Go to [GitHub PAT settings](https://github.com/settings/personal-access-tokens/) in your GitHub account and click **Generate new token**
- Configure the token with these settings:
  - **Token name**: `DAXLIBFORK_PAT`
  - **Description**: `Token for pushing changes to my DAX Lib fork` (or any description you prefer)
  - **Resource owner**: your GitHub account
  - **Expiration**: choose `No expiration` or set a date (remember to renew before expiry)
  - **Repository access**: select `Only select repositories`, then chose your forked `daxlib` repository
- Set permissions:
  - Click `+ Add permissions`
  - Select `Contents`
  - Change access level from `Read-only` to `Read and write`
- Click **Generate token**
- Copy the token (PAT) and store it securely - you won't be able to see it again once you leave the page

### 2. Add the Token to Your Repository

- Open the **Settings** tab of your new repository (the one created from this template)
- Navigate to **Secrets and variables** → **Actions** in the left sidebar
- Click **New repository secret**
- Add the secret:
  - **Name**: `DAXLIBFORK_PAT`
  - **Secret**: Paste the Personal Access Token (PAT) you created earlier
- Click **Add secret**

## 🧩 Customize Your Library

The template includes a boilerplate library called `Contoso.Sample`. Customize it for your needs:

- Update library metadata: edit `src/manifest.daxlib` to set your library's name, version and other metadata
- Add your functions: edit `src/lib/functions.tmld` to define your library's functions

## 📦 Publish Your Library

Once your code is ready, you can publish a new version:

- Go to the **Actions** tab in your repository
- Select the `publish-package` workflow from the left sidebar
- Click **Run workflow** and confirm
- Wait for the workflow to complete
- After completion, a summary will appear with a link to create a Pull Request to the official DAX Lib repository
- Click the link to open your Pull Request, add a description, and submit it for review
- If you make further changes, re-run the workflow to update the branch and the Pull Request automatically

> [!TIP]
> You can iterate on your changes as many times as needed before the pull request is merged. Just keep the same library version in `manifest.daxlib`, and each workflow run will update the same pull request.
## 📚 Resources

- [DAX Lib documentation](https://docs.daxlib.org/)
- [DAX Lib repository](https://github.com/daxlib/daxlib)
