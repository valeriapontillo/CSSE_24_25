# Capita Selecta of Software Engineering (2024/2025)

The repository hosts the material, developed and needed in the lab-sessions of CSSE, at VUB Brussels. The material is developed by Valeria Pontillo.

## Assignment 1

This assignment requires building a data set consisting of metrics that can be used for defect prediction.
We limit us to studying the Java files of one repository, [jwtk/jjwt](https://github.com/jwtk/jjwt).

We study the following revisions of the repository.

| SHA  | DATE        | AUTHOR                                                |
|-----|:--------------------------------------------------------|-------------|
| 0c2d96c2d03d2c15f6bf4789a4fca8a6e419f4d7 |2024-06-24 | lhazlewood |
| 3b529ac64013396fe2e01fcba482b4d878531cb9 |2023-10-02 | bdemers |
| 529f04dd9097331220c3239bdadacee6b1dfd6de |2023-08-04 | lhazlewood |
| 894d6f298b6edc48bddedeaa8abd930cea744f9c |2021-02-17 | Dominik Dorn |
| 56db77ed7e4b9165c0440ffc451dd813c9713578 |2019-10-03 | sal0max |
| ba1f235bd157fd3a68fc5803de65ee4d1848d5a0 |2019-02-22 | Micah Silverman |
| 54ddbedbec5a2563209028d86e5b294091f8e1c4 |2018-07-20 | Les Hazlewood |
| a473dc4be1562476df6183edf91fffa575fda21f |2017-05-13 | aadrian |
| ceac032f11ebc0bf829c68961ca3c643eb85f70e |2016-06-30 | Les Hazlewood |
| 6a422211c8a16013592cbd88d0346ebe4ca3e788 |2015-10-13 | Les Hazlewood |
| 4d2080b36973314f8ed26887addda000de84809f |2015-06-26 | Les Hazlewood |

For every revision `r`, compute the following metrics (ID) for all Java files in the repository at the particular revision.
The output file should be a CSV or line-delimited JSON file, with the columns or keys: *metric* (the ID of the metric), *value* (the value of the metric),
*file* (the path of the file), *revision* (the SHA of the revision).
The following metrics need to be extracted.

| ID  | Description                                                               |
|-----|:--------------------------------------------------------------------------|
| LOC | Number of lines of code in file `f` at a revision `r`. |
| CC  | Cyclomatic complexity in file `f` at a revision `r`. |
| NC1  | Number of commits changing file `f` **before** a revision `r`. |
| NC2  | Number of commits changing file `f` **after** a revision `r`.|
| BUG1 | Number of commits changing file `f` **before** revision `r` where the commit message includes a keyword (fix, bug ...) that indicates a defect in the file.|
| BUG2 | Number of commits changing file `f` **after** revision `r` where the commit message includes a keyword (fix, bug ...) that indicates a defect in the file.|
| DEV1 | Number of distinct developers who changed file `f` **before** a revision `r`.|
| DEV2 | Number of distinct developers who changed file `f` **after** a revision `r`.|

The code for analyzing a repository needs to be written in Python. You are encouraged to us the [gitpython](https://gitpython.readthedocs.io/en/stable/tutorial.html) library.
**The submission requires the script to compute the metrics and the CSV or line-delimited JSON file. Deadline for the assignments: 21 June 2025**
