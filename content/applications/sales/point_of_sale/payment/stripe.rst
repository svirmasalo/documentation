======
Stripe
======

Connecting a payment terminal allows you to offer a fluid payment flow to your customers and ease
the work of your cashiers.

Configuration
=============

Configure the payment method
----------------------------

Start by activating **Stripe** in the settings. From the **POS** dashboard, go to
:menuselection:`Configuration --> Settings --> Payment Terminals --> Check Stripe`.

Then, create the payment method:

- Click :menuselection:`Configuration --> Payment Methods --> Create`, and complete the
  :guilabel:`Method` field with your payment method's name;
- Set the :guilabel:`Journal` field as :guilabel:`Bank` and the :guilabel:`Use a Payment Terminal`
  field as :guilabel:`Stripe`;
- Enter your payment terminal serial number in the :guilabel:`Stripe Serial Number` field;
- Click on :guilabel:`Don't forget to complete Stripe connect before using this payment method.`

.. image:: stripe/create-method-stripe.png
   :align: center
   :alt: payment method creation form

.. note::
   - Do not check the :guilabel:`Identify Customer` field. Doing so would prevent unindentified
     customers from using Stripe.
   - The :guilabel:`Outstanding Account` and the :guilabel:`Intermediary Account` can stay empty to
     use the default accounts.
   - Find your payment terminal serial number under the device or on `Stripe's website <https://dashboard.stripe.com>`_.

Connect Stripe to Odoo
----------------------

Click on :guilabel:`Connect Stripe`. Doing so redirects you automatically to a configuration page.
Fill in all the information to create your Stripe account and link it with Odoo. Once the forms are
completed, the :guilabel:`Publishable Key` and the :guilabel:`Secret Key` are automatically loaded
in Odoo, and your terminal is ready to be used in a POS.

.. image:: stripe/stripe-connect.png
   :align: center
   :alt: stripe connect form

.. important::
   - When you use **Stripe** exclusively in Point of Sale, you only need the **Secret Key** to use
     your terminal.
   - The :guilabel:`State` is inherent to **eCommerce** and can stay set as :guilabel:`Disabled`.
   - For **On-Premise** users, the :guilabel:`Connect Stripe` button does not work. To retrieve the
     keys manually, go to `Stripe's website <https://dashboard.stripe.com>`_, log in, type
     `API` in the search bar, and click :guilabel:`Developers > API`.

Configure the payment terminal
------------------------------

Swipe right on your payment terminal, click :menuselection:`Settings --> enter the admin PIN code
--> Validate --> Network`, and select your network.

.. note::
   - The device must be connected to a secured WI-FI.
   - Your **Odoo** database and payment terminal must share the same network.
   - To access your payment terminal settings, you must enter the admin PIN code. By default, this
     code is `07139`.

Link the payment method to a POS
--------------------------------

To add a **payment method** to your point of sale, go to :menuselection:`Configuration -->
Settings`. Select the POS, go to :menuselection:`Payments --> Payment Methods`, and add your payment
method for **Stripe**.

Pay with a payment terminal
===========================

When processing a payment, select :guilabel:`Stripe` as the payment method. Check the amount and
click on :guilabel:`Send`. Once the payment is successful, the status changes to :guilabel:`Payment
Successful`. To cancel the payment request, click on :guilabel:`cancel`.

.. note::
   - | In case of connection issues between Odoo and the payment terminal, force the payment by
       clicking on :guilabel:`Force Done`, which allows you to validate the order.
     | This option is only available after receiving an error message informing you that the
       connection failed.
   - The terminal must have at least 10% battery to use it.
   - The device does not work for payments under €0.50.

Troubleshooting
===============

You cannot find the payment terminal in your Stripe account.
------------------------------------------------------------

If you cannot find a payment terminal, you need to add it manually.

#. Go to `Stripe's website <https://dashboard.stripe.com>`_, log in, and go to
   :menuselection:`Payments --> Readers --> Locations`;
#. Add a location by clicking the :guilabel:`+ New` button or select an already created location;
#. Click on the :guilabel:`+ New` button in the :guilabel:`Readers` box and fill in the required
   information.

.. note::
   You must provide a **registration code**. To retrieve that code, swipe right on your device,
   enter the admin PIN code (by default: `07319`), validate, and click on :guilabel:`Generate a
   registration code`.
