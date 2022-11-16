============================
Forecast future bills to pay
============================

In Odoo you have the possibility to manage payments by setting automatic :guilabel:`Payments Terms`
and :guilabel:`follow-ups`.

Configuration: payment terms
============================

In order to track the vendor conditions, we use :guilabel:`Payment Terms` in Odoo.
:guilabel:`Payment terms` allow keeping track of due dates on invoices. Examples of
:guilabel:`Payment Terms` are:

-  50% within 30 days
-  50% within 45 days

To create :guilabel:`Payment terms`, use the :menuselection:`Accounting app --> Configuration -->
Invoicing --> Payment Terms`. By clicking on :guilabel:`Create`, you can add the terms you need as
well as modify existing ones by clicking on it in the Payment Terms list in the same view.

Once :guilabel:`Payment Terms` are defined, you can assign them to your vendor by default.
To do so go to :menuselection:`Vendors --> Vendors` choose the :guilabel:`Vendor` you want and in
the :guilabel:`Sales & Purchase` tab you can select a specific :guilabel:`Payment Term`.
This way, every time you will purchase to this vendor, Odoo will propose you automatically the
chosen payment term.

.. note::

    If you do not set a specific payment term on a vendor, you will still be able to set a specific
    payment term on the vendor bill.

Forecast bills to pay with the Aged Payables report
===================================================

In order to track amounts to be paid to the vendors, use the Aged Payable report. You can get it
from the Reports menu of the Accounting application. This report gives you a summary per vendor of
the amounts to pay, compared to their due date (the due date being computed on each bill using the
term).
This reports tells you how much you will have to pay within the next months.

Select bills to pay
===================

Using the menu :menuselection:`Vendors --> Bills`, you can get a list of vendor bills. Using the
filters, you can list all the bills that you should pay or the bills that are overdue
(you are late on the payment).

From this screen, you can also switch to the pivot table or the graph view to get statistics on the
amount due over the next month, using the group by "Due Date" feature.
