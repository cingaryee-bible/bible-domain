# bible-domain
Automatic copy of the published daily readings at cingaryee-bible.github.io/everyday for bible.cingaryee.com.

## How publishing works

The [sync workflow](../../actions/workflows/mirror-pages.yml) checks the [published source site](https://cingaryee-bible.github.io/everyday/) every 15 minutes, on pushes to `main`, and when run manually. It publishes to [bible.cingaryee.com](https://bible.cingaryee.com/) when the copied files differ from the version already on the custom domain.

Edit the daily readings in [cingaryee-bible/everyday](https://github.com/cingaryee-bible/everyday). Once the source site publishes the change, the next successful sync can copy it to the custom domain.

## Check or restart syncing

1. Open the [sync workflow](../../actions/workflows/mirror-pages.yml) and check the latest scheduled run. If the site is already synchronized, the publishing steps are skipped.
2. If GitHub has disabled the workflow after 60 days of repository inactivity, select **Enable workflow**.
3. To check for updates immediately, select **Run workflow** on `main` and review the result.
