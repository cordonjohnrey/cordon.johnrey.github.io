# Email Preference Reverts After Reload

This is a practice bug report for a fictional e-commerce app. The environment and results are simulated.

| Field | Details |
| --- | --- |
| ID | DEMO-014 |
| Area | Account settings |
| Environment | Demo staging build 0.4.2, Chrome on Windows 11 |
| Frequency | 3 out of 3 attempts with the same test account |
| Suggested severity | Medium. Customers can’t reliably update an email preference. |

## Steps to reproduce

1. Sign in to a test account with **Product updates** turned on.
2. Open **Account → Email preferences**.
3. Turn **Product updates** off and click **Save changes**.
4. Wait for the “Preferences saved” message, then reload the page.
5. Check the **Product updates** toggle.

## Expected result

**Product updates** stays off after reloading the page.

## Actual result

The app says “Preferences saved,” but **Product updates** is back on after reload. The test only confirmed what the settings page displays. Whether product emails would still be sent needs a separate check.

## Retest after the fix

Save the preference as off, then reload the page and sign out and back in to confirm it stays off. Turn it on again and repeat the check to verify the setting saves both ways.
