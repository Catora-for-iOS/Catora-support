# Catora User Guide

**Simple Monthly Budgeting for iPhone, iPad and Mac**

**Last updated:** 5 October 2026

Catora is a personal budgeting and record-keeping app. It helps you record income, assign that money to categories, enter spending, plan future months, manage repeating payments and review spending trends. It does not connect to a bank or move real money.

## A simple way to get started

1. Open **Income** and add a paycheck, deposit or other money received.
2. Open **Categories** and assign the available money to the things you plan to spend it on.
3. Open **Transactions** whenever you spend money.
4. Check **Overview** to see what remains, spot overspending and review upcoming repeating payments.
5. Create a JSON backup after important changes using the backup controls described below.

## Moving around Catora

Catora has four main areas: **Overview**, **Transactions**, **Categories** and **Income**. iPhone shows them in a tab bar. iPad and Mac use a sidebar when there is enough space. On Mac, Command-1 through Command-4 also switch between them.

The month control appears near the top of each area. Use its arrows to move backward or forward by one month. The selected month is shared across the app, so changing it on one tab changes it everywhere.

Catora does not automatically sync the active budget between devices. To transfer a budget yourself, create a JSON backup and restore it on the other device after reviewing the replacement.

Currency symbols and number formatting follow the device's region settings. Changing region changes how saved amounts are displayed; it does not convert them into another currency.

## Overview

Overview is the dashboard for the selected month.

### Summary figures

- **Left to Spend from Budget** is the money currently available across categories, including balances carried forward from earlier months.
- **Left in Account** is all income received through the selected month minus all spending through that month.
- **Assigned this month**, **Spent this month** and **Income this month** show activity within the selected month.
- **Ready to Assign** is recorded income that has not yet been assigned to categories. For the current and future months it also reserves assignments already planned in later months.
- **Overspent Categories** appears when a category's available amount is below zero. Select a listed category to edit it or move money into it.

### Repeating Left to Pay

This card totals active repeating payments still due after today in the selected month. Select it to open **Repeating Transactions** on the Transactions tab. A historical month has no upcoming payments.

### Spending Trends

Select the **Spending Trends** card to open a larger chart.

- Choose **6 Months** or **12 Months**.
- Choose all categories or one category, including an archived category.
- Select a bar to inspect a month's spending.
- Trends use actual transactions only. Category assignments and transfers are not spending and are not included.

### Overview actions and settings

On iPhone and iPad, open the **Overview** ellipsis menu. **Manage Data…** appears under **Data**. On Mac, the **File** menu contains backup, restore, earlier-version, CSV and reset commands; the **Data** toolbar menu also provides backup, restore, earlier-version and CSV commands. Use **Catora ▸ Settings…** for appearance and App Lock, **Catora ▸ About Catora** for app information, and the **Help** menu for the user guide, support and privacy policy.

- **Require Device Authentication** turns App Lock on or off. Apple system authentication may use Face ID, Touch ID or the device passcode on iPhone and iPad, or available Touch ID or your Mac login password on macOS. Catora receives only whether authentication succeeded or failed.
- **Appearance** changes the color theme and heading style.
- **Privacy & About** shows the app version and build, privacy information, support links and important data-handling notes.

### Backups

On iPhone and iPad, open **Overview ▸ ellipsis ▸ Manage Data…** (under **Data**), then **Backups**. On Mac, use the **File** menu or **Data** toolbar menu.

- **Create Backup** on iPhone and iPad, or **File ▸ Back Up…** on Mac, saves a portable JSON copy of categories, assignments, transfers, transactions, income and repeating-transaction rules to a location you choose.
**Restore a Backup** is a two-step process:

1. Select **Choose Backup** on iPhone or iPad, or **File ▸ Restore from Backup…** on Mac, to open a saved backup. Catora validates it and shows its filename and record counts.
2. Review the selected file, then confirm **Restore Backup**. Only then does it replace the active budget. The previous active budget is kept as a local automatic recovery snapshot.

On Mac, **File ▸ Earlier Versions…** lets you inspect and restore local automatic recovery versions after confirmation. Automatic snapshots and the previous local copy help recover changes; they are stored on this device and are not a substitute for a separately saved backup.

Keep separately saved backup files secure. They remain in their saved location until you delete them there.

### Reset

On iPhone and iPad, choose **Reset…** from the **Overview** ellipsis menu. On Mac, choose **File ▸ Reset Budget…**. Reset is destructive and asks for confirmation.

- **Start Fresh** replaces the active budget with Catora's normal starter categories and no money assigned.
- **Start Again with Sample Data** replaces it with a small example budget to explore.
- Appearance and App Lock settings remain unchanged.
- Reset removes Catora's local automatic recovery versions. The app warns if cleanup cannot be completed. Separately saved backups and CSV files remain until you delete them from their saved location.

## CSV Import and Export

On iPhone and iPad, open **Overview ▸ ellipsis ▸ Manage Data…** (under **Data**), then **CSV Import & Export**. On Mac, use **File ▸ Import CSV…** or **File ▸ Export CSV…** (also available in the **Data** toolbar menu).

CSV exchanges transactions and income with spreadsheet software. Import appends approved rows and never replaces the current budget. Export saves to the file location or storage provider you select.

### File format

Use a UTF-8 CSV file with this header:

```csv
date,type,payee_or_source,category,amount,note
```

- **date**: a real Gregorian date in **YYYY-MM-DD** format.
- **type**: **transaction** or **income**.
- **payee_or_source**: required payee or income source.
- **category**: required for transactions; empty for income.
- **amount**: a decimal using a period, with at most two decimal places and no currency symbol or grouping separator. Negative transaction amounts represent refunds; income amounts must be non-negative.
- **note**: optional.
- Quote fields containing commas, quotes or line breaks using standard CSV double-quote escaping.
- Exported text beginning with **=**, **+**, **-** or **@** receives a protective apostrophe to prevent spreadsheet formula execution. Catora removes its protective apostrophe when importing that CSV again.

### Review an import

1. Select the CSV file. Catora parses the entire file before changing your budget.
2. Review invalid rows, categories needing a choice and possible duplicates. Possible duplicates are excluded unless you explicitly include them.
3. Resolve the review choices and approve the rows to append. Catora saves approved rows together after validation. Cancelling or a failed validation or save leaves your existing budget unchanged.

CSV includes transaction and income values only. It does not preserve monthly assignments, budget transfers, repeating rules, category order or archive state, or app settings. Use a JSON backup for a complete restorable budget copy.

CSV files may contain sensitive financial information. Catora reads or writes only files you select and does not upload their contents to a developer server. Keep exported files secure; they remain at your chosen location or storage provider until you delete them.

## Transactions

Transactions records money spent during the selected month. Entries are grouped by date with the newest dates first.

### Find and filter transactions

- Type in **Search transactions** to search payee, note, category, amount or date.
- Use the category filter to show one active or archived category.
- Use **Clear Search**, **Clear Filters** or **Clear All Filters** to return to the full list.
- On iPhone and iPad, **Cancel** clears the search and dismisses the keyboard; the keyboard’s **Search** key dismisses it while keeping your results.

### Add a transaction

Select **New Transaction** and complete:

- **Payee** — entering a previous payee may show suggestions and preselect its most recently used active category.
- **Amount** — enter a positive amount and choose Expense or Refund. Refunds are recorded as one-off transactions and cannot repeat.
- **Category** — a transaction needs an active category. If there are none, add one on Categories first.
- **Date** — determines which month and day contains the transaction.
- **Note** — optional extra detail.
- **Repeats** — optionally create a weekly, every-two-weeks, monthly or yearly series beginning with this transaction.

Tap an existing transaction on iPhone or iPad, or double-click its row on Mac, to edit or delete it. Deleting updates the category balance and cannot be undone. Editing a transaction already created by a repeating series changes that occurrence only.

### Repeating Transactions

Open the repeat icon in the Transactions toolbar. The list is ordered by the next due date.

- Tap a series on iPhone or iPad, or double-click its row on Mac, to edit its payee, amount, category, frequency, due day, note and **Active** status.
- Turn **Active** off to pause future generation. Resuming creates missed occurrences from the last recorded date using the saved rule.
- Monthly and yearly schedules set to a day that a month does not have use that month's final day.
- Delete a series to stop future occurrences. Transactions already generated remain in history.

## Categories

Categories is where income becomes a plan. Each active category card shows the amount available after carried-forward money, this month's assignment and spending.

### Budget summary

- **Left to Budget** is the selected month's Ready to Assign amount.
- **Assigned this month** is the total assigned across categories for that month.

### Category Actions

Open the plus or **Category Actions** menu.

- **Add Category** creates a category and optionally assigns money for the selected month.
- **Move Money Between Categories** moves an amount without changing income or spending.
- **Copy Previous Month's Budget** replaces the selected month's category assignments with the previous month's assignments. If the selected month already has assignments, Catora asks for confirmation first.

### Work with category cards

- Select a card to edit its name and selected-month assignment and to see carried forward, spent and available totals.
- Drag one active card onto another to reorder it. On touch devices, touch and hold before dragging.
- From the editor, move money to or from the category.
- Archive a category when it is no longer used. Historical transactions and assignments remain attached, but the category is unavailable for new spending or assignments. Catora may require a deficit to be resolved before archiving.
- Unarchive a category to use it again.
- A category can be permanently deleted only when it has no history that must be preserved.

### Move Money

- Choose **Ready to Assign** or an eligible category as the source.
- Choose an active category as the destination.
- Enter an amount, or use the quick minus/plus 1 and 10 controls.
- Review the projected balances under **After Moving**, then select **Move**.
- Catora will not move more than the source currently has available.

## Income

Income records money received during the selected month. Entries are grouped by date with the newest dates first.

### Find income

Use **Search income** to filter the list. On iPhone and iPad, **Cancel** clears the search and dismisses the keyboard; the keyboard’s **Search** key dismisses it while keeping your results. Use **Clear Search** to return to the full list.

### Add income

Select **New Income** and enter:

- **Source** — for example salary, freelance work or a gift.
- **Amount** — the positive amount received.
- **Date** — determines the month and day of the entry.
- **Note** — optional extra detail.

Tap an existing entry on iPhone or iPad, or double-click its row on Mac, to edit or delete it. Deleting income updates the budget totals and cannot be undone.

## If Catora cannot open its saved budget

Catora preserves the existing files and shows **Budget Recovery** instead of silently replacing them. You can choose a valid backup to restore or explicitly start fresh. When restoring over an unreadable budget, the unreadable file is preserved separately.

## Privacy and support

Catora keeps its active financial data and automatic recovery copies in the app's local storage and does not send that data to a developer server. JSON backups and CSV exports go only to the location you choose. Keep them secure and delete them separately when no longer needed.

- Read the [Privacy Policy](privacy.html).
- Visit [Catora Support](support.html) or email **Catora.support@gmail.com**.
- Return to the [Catora home page](index.html).

