Type: #atom
Atom: [[Date and Time Series (pd)]]
Topic: Quant 
Understanding: #Exploratory 

----
# Overview

**Resampling** - We can call the `.resample()` method on a Series or DataFrame with a `DateTimeIndex` to return a `Resampler` object which functions similar to a `GroupBy` object - we can call some aggregation function like `.first()` on it.

**Shifting** - We've seen this.

# Dates and Times

There are 4 kinds of time-related index objects in Pandas: `DateTimeIndex`, `TimedeltaIndex`, `PeriodIndex`. We will focus only on the first one.

Date Range - We can create a `DateTimeIndex` with `pd.date_range(...)`. Inputs can be a Python `datetime.datetime(...)` object, a string, int or float
Scalar Timestamp - We can create a `TimeStamp` with `pd.Timestamp(...)`.