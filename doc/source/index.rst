yfinance documentation
======================

Download Market Data from Yahoo! Finance's API
----------------------------------------------

.. admonition:: IMPORTANT LEGAL DISCLAIMER

   **Yahoo!, Y!Finance, and Yahoo! finance are registered trademarks of Yahoo, Inc.**

   yfinance is **not** affiliated, endorsed, or vetted by Yahoo, Inc. It's
   an open-source tool that uses Yahoo's publicly available APIs, and is
   intended for research and educational purposes.

   **You should refer to Yahoo!'s terms of use**
   (`here <https://policies.yahoo.com/us/en/yahoo/terms/product-atos/apiforydn/index.htm>`__),
   (`here <https://legal.yahoo.com/us/en/yahoo/terms/otos/index.html>`__),
   and (`here <https://policies.yahoo.com/us/en/yahoo/terms/index.htm>`__)
   for details on your rights to use the actual data downloaded.
   Remember - the Yahoo! finance API is intended for personal use only.

.. .. toctree::
..    :maxdepth: 3
..    :hidden:
..    :titlesonly:

.. toctree::
   :maxdepth: 1
   :hidden:
   :titlesonly:

   user_guide/index
   reference/index
   development/index

Quick Start
-----------

.. code-block:: bash

    $ pip install yfinance

.. code-block:: python

   import yfinance as yf

   dat = yf.Ticker("MSFT")

   # get historical market data
   dat.history(period='1mo')

   # options
   dat.option_chain(dat.options[0]).calls

   # get financials
   dat.balance_sheet
   dat.quarterly_income_stmt

   # dates
   dat.calendar

   # general info
   dat.info

   # analysis
   dat.analyst_price_targets

That's just a sample - see :doc:`user_guide/index` or :doc:`reference/index` for everything.
