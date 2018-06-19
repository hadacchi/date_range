# date_range

return generator from t0 to t1 every dt.

This function returns a range generator of datetime object.

Parameters
----------
    t0 : datetime.datetime
         A datetime object. A generator start from t0.
    t1 : datetime.datetime
         A datetime object. Datetime objects which the generator returns will
         increase until t1. t1 is never returned.
    dt : datetime.timedelta
         A timedelta object. Datetime objects which the generator returns will
         increase every dt.

Examples
--------
    >>> type(date_range(datetime(2018,1,1), datetime(2018,1,4)))
    <class 'generator'>
    >>> list(date_range(datetime(2018,1,1), datetime(2018,1,4)))
    [datetime.datetime(2018, 1, 1, 0, 0), datetime.datetime(2018, 1, 2, 0, 0), datetime.datetime(2018, 1, 3, 0, 0)]
    >>> list(date_range(datetime(2018,1,1,10), datetime(2018,1,1,11), timedelta(seconds=600)))
    [datetime.datetime(2018, 1, 1, 10, 0), datetime.datetime(2018, 1, 1, 10, 10), datetime.datetime(2018, 1, 1, 10, 20), datetime.datetime(2018, 1, 1, 10, 30), datetime.datetime(2018, 1, 1, 10, 40), datetime.datetime(2018, 1, 1, 10, 50)]
