---
layout: post
title: Group project 1
due: "Feb 27, 11:59pm"
categories: [assignments]
---

# Group project 1

Using [Backblaze's hard drive data](https://www.backblaze.com/hard-drive-test-data.html) (2014 only), convince me of the following:

- Some manufacturer produced particularly bad drives of a certain size (in TB). Convince me by graphing annual failure rate (AFR) for different manufacturers and drive sizes. Get the manufacturer by taking the first two characters of the model name. Bin the drive sizes into TB units (using `cut` as shown in our [R cookbook](/cookbook/r.html)). Calculate AFR according to the `stats.sql` file that comes with the dataset. Calculate AFR entirely in R, do not use the SQL queries.

- Drives of a certain TB size-range (e.g., 3-4TB) do or do not have a higher proportion of failures than other sizes. Use `prop.test` from our [statistics notes](/notes/statistics.html), comparing failure counts vs. number of drives in operation for various sizes.

- The hard disk SMART stat #187 (raw form, not normalized), which measures read errors, is strongly positively correlated with disk failure. First convert the SMART measure into distinct levels like 0, 1-3, 3-6, 6-11, etc. using the `cut` command as above. Show an actual correlation value, of the SMART levels with AFR, and interpret the correlation value.

Each group should have exactly two people. Create one Bitbucket repository and add me as a reader. I will look at the commits to grade each person separately; you should both do equal amounts of work. Please only share notes with your group partner. I want everyone to think creatively about how to complete the task.

Create a report in RMarkdown (or R LaTeX). Do not "echo" all the commands, rather, just report the interesting bits. Write a little bit of narrative (a few sentences or whatever's needed) to make sense of the data/plots you show.

 **Do not add the CSV files to the repository. I do not need duplicates of a 3GB dataset!** Do not download the data on delenn. The data already lives on delenn at `/bigdata/data/backblaze`.

 Please do add the rendered report (in PDF or HTML) to your repository so I don't have to wait to render every report.

