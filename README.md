# UoT_SkillTest
## **Part 1**
## **Part 2**
1. Find the oldest book for each author.
<code>
SELECT
  "AUTHOR FIRST NAME",
  "AUTHOR LAST NAME",
  "TITLE",
  "PUBLISHED DATE"
FROM
  your_table
WHERE
  ("AUTHOR FIRST NAME", "AUTHOR LAST NAME", "PUBLISHED DATE") IN (
    SELECT
      "AUTHOR FIRST NAME",
      "AUTHOR LAST NAME",
      MIN("PUBLISHED DATE")
    FROM
      your_table
    GROUP BY
      "AUTHOR FIRST NAME",
      "AUTHOR LAST NAME"
  );
</code>
