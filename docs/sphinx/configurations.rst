..
    This file is part of BDC-STAC.
    Copyright (C) 2022 INPE.

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program. If not, see <https://www.gnu.org/licenses/gpl-3.0.html>.

.. _conf:

Service Configuration
=====================


.. data:: SQLALCHEMY_DATABASE_URI

   The database URI that should be used for the database connection. Defaults to ``'postgresql://postgres:postgres@localhost:5432/bdc'``.


.. data:: SQLALCHEMY_TRACK_MODIFICATIONS

    Enable (True) or disable (False) signals before and after changes are committed to the database. Defaults to ``False``.


.. data:: SQLALCHEMY_ECHO

   Enables or disable debug output of statements to ``stderr``. Defaults to ``False``.


.. data:: SQLALCHEMY_ENGINE_OPTIONS

    Set SQLAlchemy engine options for pooling and recycle.
    You may set the following environment variables to customize pooling:

    - ``SQLALCHEMY_ENGINE_POOL_SIZE``: The pool size. Defaults to ``5``.
    - ``SQLALCHEMY_ENGINE_MAX_OVERFLOW``: Max pool overflow. Defaults to ``10``.
    - ``SQLALCHEMY_ENGINE_POOL_CLASS``: The pool type for management. Defaults to ``10``.
    - ``SQLALCHEMY_ENGINE_POOL_RECYCLE``: Define the given number of seconds to recycle pool. Defaults to ``-1``, or no timeout.

.. data:: BDC_STAC_BASE_URL

    The base URI of the service. Defaults to ``'http://localhost:5000'``.


.. data:: BDC_STAC_FILE_ROOT

    The prefix for image ``assets``. Defaults to ``'http://localhost:5001'``.

    This value is ignored if ``X-Script-Name`` is present in ``request.headers``.


.. data:: BDC_STAC_MAX_LIMIT

    The limit of items returned in a query. Defaults to `1000` (an integer value).


.. data:: BDC_AUTH_CLIENT_ID

    Client ID generated by BDC-Auth. Defaults to ``None``, that means only public collections will be returned.



.. data:: BDC_AUTH_CLIENT_SECRET

    Client secret generated by BDC-Auth. Defaults to ``None``, that means only public collections will be returned.


.. data:: BDC_AUTH_ACCESS_TOKEN_URL

    Access token url used for retrieving user info in BDC-Auth. Defaults to ``None``, that means only public collections will be returned.


.. data:: BDC_STAC_USE_FOOTPRINT

    Flag to set if Item intersection should use ``Item.footprint``. Defaults to ``0``, which means to use ``Item.bbox``.

