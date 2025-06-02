# Adding Origitech NuGet Package Source in Visual Studio

## 1. Create a GitHub Classic Token

Follow GitHub's guide to [create a personal access token (classic)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) with the following permission:

- `read:packages`

> ⚠️ You can set the token with no expiration date, but **make sure the scope is limited to `read:packages` only** for security reasons.

---

## 2. Add Origitech Package Source

Use your newly created token to add the Origitech package source to your NuGet configuration.

> 🔐 Replace `GITHUB_TOKEN` with your actual token.  
> 👤 `USERNAME` can be left as-is — it's not relevant when using tokens.

### Option A: Using `dotnet` CLI

```powershell
dotnet nuget add source --username USERNAME --password GITHUB_TOKEN --name Origitech "https://nuget.pkg.github.com/Origitech/index.json"
