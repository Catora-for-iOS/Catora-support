# Catora User Guide

**Simple Monthly Budgeting for iPhone, iPad and Mac**

Catora is a personal budgeting and record-keeping app. It helps you record income, assign that money to categories, enter spending, plan future months, manage repeating payments and review spending trends. It does not connect to a bank or move real money.

## A simple way to get started

1. Open **Income** and add a paycheck, deposit or other money received.
2. Open **Categories** and assign the available money to the things you plan to spend it on.
3. Open **Transactions** whenever you spend money.
4. Check **Overview** to see what remains, spot overspending and review upcoming repeating payments.
5. Use **Create Backup** from Overview after important changes.

## Moving around Catora

Catora has four main areas: **Overview**, **Transactions**, **Categories** and **Income**. iPhone shows them in a tab bar. iPad and Mac use a sidebar when there is enough space. On Mac, Command-1 through Command-4 also switch between them.

The month control appears near the top of each area. Use its arrows to move backward or forward by one month. The selected month is shared across the app, so changing it on one tab changes it everywhere.

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

On iPhone and iPad, open the ellipsis menu. On Mac, **Backup**, **Settings** and **Reset** are separate toolbar menus.

- **Require Device Authentication** turns App Lock on or off. Apple system authentication may use Face ID, Touch ID or the device passcode. Catora receives only whether authentication succeeded or failed.
- **Appearance** changes the color theme and heading style.
- **Privacy & About** shows the app version and build, privacy information, support links and important data-handling notes.

### Backups

Open **Manage Backups** from Overview.

- **Create Backup** saves a portable JSON copy of categories, assignments, transfers, transactions, income and repeating-transaction rules to a location you choose.
- **Choose Backup** opens a saved backup. Catora validates it and shows record counts before anything is replaced.
- **Restore Backup** replaces the active budget only after confirmation. The previous active budget is kept as a local automatic recovery snapshot.
- Keep separately saved backup files secure. They remain in their saved location until you delete them there.

### Reset

Reset is destructive and asks for confirmation.

- **Start Fresh** replaces the active budget with Catora's normal starter categories and no money assigned.
- **Start Again with Sample Data** replaces it with a small example budget to explore.
- Appearance and App Lock settings remain unchanged.
- A local recovery copy and separately saved backups may remain, so Reset is not a guarantee that every copy has been deleted.

## Transactions

Transactions records money spent during the selected month. Entries are grouped by date with the newest dates first.

### Find and filter transactions

- Type in **Search transactions** to search payee, note, category, amount or date.
- Use the category filter to show one active or archived category.
- Use **Clear Search**, **Clear Filters** or **Clear All Filters** to return to the full list.

### Add a transaction

Select **New Transaction** and complete:

- **Payee** — entering a previous payee may show suggestions and preselect its most recently used active category.
- **Amount** — enter the positive amount spent.
- **Category** — a transaction needs an active category. If there are none, add one on Categories first.
- **Date** — determines which month and day contains the transaction.
- **Note** — optional extra detail.
- **Repeats** — optionally create a weekly, every-two-weeks, monthly or yearly series beginning with this transaction.

Select an existing transaction to edit or delete it. Deleting updates the category balance and cannot be undone. Editing a transaction already created by a repeating series changes that occurrence only.

### Repeating Transactions

Open the repeat icon in the Transactions toolbar. The list is ordered by the next due date.

- Select a series to edit its payee, amount, category, frequency, due day, note and **Active** status.
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

### Add income

Select **New Income** and enter:

- **Source** — for example salary, freelance work or a gift.
- **Amount** — the positive amount received.
- **Date** — determines the month and day of the entry.
- **Note** — optional extra detail.

Select an existing entry to edit or delete it. Deleting income updates the budget totals and cannot be undone.

## If Catora cannot open its saved budget

Catora preserves the existing files and shows **Budget Recovery** instead of silently replacing them. You can choose a valid backup to restore or explicitly start fresh. When restoring over an unreadable budget, the unreadable file is preserved separately.

## Privacy and support

Catora keeps its active financial data and automatic recovery copies in the app's local storage and does not send that data to a developer server. Files created with **Create Backup** go only to the location you choose.

- Read the [Privacy Policy](privacy.html).
- Visit [Catora Support](support.html) or email **Catora.support@gmail.com**.
- Return to the [Catora home page](index.html).
