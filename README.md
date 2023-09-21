# [Spark Challenge] 
Module 22

**NOTE - The code must be run using** [Google Colab](https://colab.google/). 

## TABLE OF CONTENTS

1. Overview
2. Summary
3. Installation
4. Contributing
5. Acknowledgements
6. Licenses

## 1. Overview:

In this challenge, [Apache Spark](https://en.wikipedia.org/wiki/Apache_Spark) was used to determine key metrics about home sales data. Spark was employed to create a [temporary view](https://spark.apache.org/docs/3.0.0-preview/sql-ref-syntax-ddl-create-view.html), partition the data, [cache](https://en.wikipedia.org/wiki/Cache_(computing)) and uncache a temporary table, and verify that the table had been uncached.

The temporary view was used several times to query and tabulate data using [SparkSQL](https://spark.apache.org/sql/). But another crucial parts of the assignment  was comparing [runtime](https://en.wikipedia.org/wiki/Runtime_(program_lifecycle_phase)) length between cached data and [Parquet](https://en.wikipedia.org/wiki/Apache_Parquet) data. This is probably because, when dealing with [huge datasets](https://en.wikipedia.org/wiki/Big_data), storing and retrieving data the optimal way is important.

Caching is storing a [dataframe](https://spark.apache.org/docs/1.6.3/api/java/org/apache/spark/sql/DataFrame.html), which happens in [memory](https://en.wikipedia.org/wiki/Computer_data_storage). Parquet is about saving a "parqued" file, which happens on [disk](https://en.wikipedia.org/wiki/Disk_storage). In columnar storage like Parquet, data is stored by columns, not rows (e.g., [.csv](https://en.wikipedia.org/wiki/Comma-separated_values#:~:text=Comma%2Dseparated%20values%20(CSV),typically%20represents%20one%20data%20record.)), allowing the system to efficiently read the values of a specific column without the need to scan through unrelated data. This is particularly useful when the user has a specific query. (This begs the question: _why, if columnar data is so efficient, isn't it always in use?_ The answer is that it's more difficult to "eyeball" than a typical relational, row-based table, and using columns for all but the most giant files won't save resources anyway.)

It should be noted that when data is read for the first time (and it isn't cached yet), reading from a Parquet file can be faster than reading from less efficient file formats due to the benefits of columnar storage (e.g., greater ability to compress the data). However, once data is cached in memory, subsequent reads will generally be faster than reading from any disk-based storage, including Parquet.

## 3. Installation:

- Code file: **Home_Sales_colab.ipynb** -- **NOTE: The code must be run using** [Google Colab](https://colab.google/). **_This is very important._**
- The assignment details and starter code are proprietary and located on the [Rutgers University](https://www.rutgers.edu/) [(edX)](https://www.edx.org/) Bootcamp Spot [Module 22 Challenge](https://bootcampspot.instructure.com/courses/3337/assignments/54019?module_item_id=962092) webpage.
- This project was created on a [PC](https://en.wikipedia.org/wiki/Personal_computer) using [Google Chrome](https://www.google.com/chrome/) for [Windows](https://www.microsoft.com/en-us/windows) version 115.0.5790.102 and its associated [Google DevTools](https://developer.chrome.com/docs/devtools/) extension. **If the program doesn't function, it is recommended that the user attempt running it on this platform and browser.**
- Coding was guided by the [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) ("Don't Repeat Yourself") principle.

## 4. Contributing:

- Andi Mysllinj 

## 5. Acknowledgements:

In addition to using the resources listed above, the author acquired query responses in OpenAI's [ChatGPT](https://chat.openai.com/) app versions 3.5 and 4, and the [VSCode GitHub Copilot](https://github.com/features/copilot) app V1.

The author also consulted code and results from similar projects publicly accessible in [GitHub](https://github.com/) repositories and recoverable through [Google](https://www.google.com/) and comparable search engines:

- [brianmslee](https://stackoverflow.com/users/20086392/brianmslee) [sic]: April 2023. [Home-Sales-Big-Data-with-PySpark-SQL](https://github.com/brianmslee/Home-Sales-Big-Data-with-PySpark-SQL)
- [Heidari, Ali T.](https://www.linkedin.com/in/theidari/): Toronto, Ontario, Canada, April 2023. [home_sales](https://github.com/theidari/home_sales)
- [Sultani, Farrukh](https://www.linkedin.com/in/farrukh-sultani-b5583060/): California, USA, May 2023. [Home_Sales](https://github.com/FarrukhSultani/Home_Sales)

## 6. Licenses:

- This program is allowed for free use via the [Creative Commons Zero v1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) license


** Worked with Adam Glantz on this challenge**
