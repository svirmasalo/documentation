===========================================
Do a year end in Odoo (close a fiscal year)
===========================================

Before going ahead with closing a fiscal year, there are a few steps one should typically take to
ensure that your accounting is correct, up-to-date, and accurate:

-  Make sure you have fully reconciled your **bank account(s)** up to year-end and confirm that your
   ending book balances match your bank statement balances.

-  Verify that all :guilabel:`Customer Invoice` have been entered and approved and that there are no
   more draft invoices.

-  Confirm that you have entered and agreed on all :guilabel:`Vendor bills`.

-  Validate all :guilabel:`Expenses`, ensuring their accuracy.

-  Corroborate that all :guilabel:`Received payments` have been encoded and recorded accurately.

-  Close :guilabel:`Suspense accounts`.

-  Book all the :guilabel:`Depreciation` and :guilabel:`Deferred Revenues`.

Year-end checklist
==================

- Run a :guilabel:`Tax report`, and verify that your tax information is correct.

- Reconcile all accounts on your :guilabel:`Balance Sheet`:

 - Update your bank balances in Odoo according to your actual bank balances on your statements.

 - Reconcile all transactions in your cash and bank accounts by running your
   :guilabel:`Aged Receivables` and :guilabel:`Aged Payables` reports.

 - Audit your accounts, being sure to fully understand the transactions affecting them and the
   nature of the transactions, making sure to include loans and fixed assets.

- Run the optional :guilabel:`Payments Matching` feature under the :guilabel:`More` dropdown on the
  dashboard, validating any open :guilabel:`Vendor Bills` and :guilabel:`Customer Invoices` with
  their payments. This step is optional, however it may assist the year-end process if all
  outstanding payments and invoices are reconciled, and could lead finding errors or mistakes in the
  system.

- Your accountant/bookkeeper will likely verify your balance sheet items and book entries for:

 - Year-end manual adjustments.

 - **Work in Progress**.

 - **Depreciation Journal Entries**.

 - **Loans**.

 - **Tax adjustments**.

If your accountant/bookkeeper is going through end of the year auditing, they may want to have paper
copies of all balance sheet items (such as loans, bank accounts, prepayments, sales tax statements,
etc...) to compare these with your Odoo balances.

During this process, it is good practice to set the :guilabel:`Lock date for Non-Advisers` to the
last day of the preceding financial year, which is set under the accounting configuration. This way,
the accountant can be confident that nobody is changing the previous year transactions while
auditing the books.

.. warning::
  On this screen, you also have a field :guilabel:`all users Lock date`. This lock date will
  prevent journal entries creation prior to the defined date for all users.
  This lock date is irreversible and cannot be removed.

.. note::
  The :guilabel:`all journal Lock date` prevents journal entry creation or modification prior the
  defined date except for advisor users.
  This lock date is reversible and can be removed.

Closing the fiscal year
=======================

There is no need to do a specific year end closing entry in order to close out your
:guilabel:`Profit and Loss statement`.
The reports are created in real-time, meaning that your :guilabel:`Profit and Loss statement`
corresponds directly with the year end-date you specify in Odoo. Therefore, any time you generate
the :guilabel:`Income Statement`, the beginning date will correspond with the beginning of the
:guilabel:`Fiscal Year` and the account balances will all be 0.

Once the accountant/bookkeeper has created the journal entry to allocate the
:guilabel:`Current Year Earnings`, you should set the :guilabel:`Lock Date` to the last day of the
fiscal year. Making sure that before doing so, you confirm whether or not the current year earnings
in the :guilabel:`Balance Sheet` is correctly reporting a balance of 0.

.. seealso::
   - :doc:`fiscal_year`