=============================
Acquiring Data For Tracktable
=============================

"Internal" to Tracktable
========================
Sample test data files are provided in the ``tracktable-data`` python package located on PyPi and Conda-Forge.
These test data files are used for Tracktable's internal tests and provide a good representation of the
type of data that can be processed by Tracktable. Usage of the ``tracktable-data`` retrevial function
can be seen below:

.. code-block:: python
   :caption: Retrieving Sample Data
   :linenos:

   from tracktable_data.data import retrieve
   from tracktable.rw.load import load_trajectories

   # Retrieve data by filename
   filepath = retrieve(filename='SampleFlight.csv')

   # Once we have file path is the file can be loaded
   trajectories = load_trajectories(filepath)

.. todo:: When the "super-duper example data file" is created update this section with it's location.

External to Tracktable
======================

Below are data resources that can provide data for Tracktable to process. This is by
no means a comprehensive list of resources but rather a springboard for real world data
compatiable with Tracktable.

.. tip:: The Tracktable library is designed to process large datasets,
   so the larger the dataset used the better results Tracktable will produce.

Air Traffic
-----------
- `Opensky <https://opensky-network.org/>`_
- `ADS-B Exchange <https://www.adsbexchange.com/>`_
- `FlightAware <https://flightaware.com/>`_

    .. note:: A subscription is required to aquire data from FlightAware
- `AirNav <https://www.airnav.com/>`_

    .. note:: A subscription is required to aquire data from AirNav

Maritime Traffic
----------------
- `AISHub <http://www.aishub.net/>`_
- `Marine Cadastre <https://marinecadastre.gov/>`_
- `Marine Traffic <https://www.marinetraffic.com/en/p/services>`_

    .. note:: A subscription is required to aquire data from Marine Traffic

Vehicle Traffic
---------------
- `New York City Taxi Data <https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page>`_

.. tip:: Tracktable also includes a random trajectory generator! Take a look at the
    Python Data Generation Example.