# PSV website

## Automatic Eredivisie standings

The public website reads its standings from `stand.json`. GitHub Actions refreshes this file every six hours using the Eredivisie endpoint from [football-data.org](https://www.football-data.org/).

To enable updates:

1. Create a free football-data.org account and copy your API token.
2. In the `psv-projectkoen-site` GitHub repository, open **Settings → Secrets and variables → Actions**.
3. Add a repository secret named `FOOTBALL_DATA_API_KEY` with your token as its value. Do not put the token in website files or commit it.
4. Open **Actions → Update Eredivisie standings → Run workflow** to publish the first standings snapshot. After that, GitHub updates the database every six hours.