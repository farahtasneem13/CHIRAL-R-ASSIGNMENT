# CHIRAL-R-ASSIGNMENT
# load packages
library (tidyverse)
library (readxl)
library(gtsummary)
library(gt)


# load data
data <- read_excel("raw_data/AMR_KAP_Data.xlsx")


install.packages("gtsummary")

# table 1
data |>
  select(1:11) |>
  tbl_summary()|>
  as_gt()|>
  gtsave("tables/Table1.docx")

  
# table 2
data |>
  select(41:49) |>
  tbl_summary()|>
  as_gt()|>
  gtsave("tables/Table2.docx")
  
