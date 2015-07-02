# text_sql
A set of SQL query similiar commands to deal with text(TSV) as structured database table


COMMAND LIST:
--------------------------------------------------------
## tjoin
Partial text match join in the specified column. An interesting use case is to perform a Chinese word segmentation.

	Usage: ./tjoin DICTION_FILE [DICTION_COLUMN [SOURCE_COLUMN [MODE [POSITION]]]]

    MODE can take values of:
        1   OR
        2   AND
        3   SUBSTRACT

    POSITION can take values of:
        0  default value, match anywhere
        1  match the head of the field
        2  match the tail of the field

## pjoin
Whole column match join, similiar to join operator in SQL

	Usage: ./pjoin DICTION_FILE [DICTION_COLUMN [SOURCE_COLUMN [MODE]]]

    MODE can take values of:
        1   OR
        2   AND
        3   SUBSTRACT

	If a Cartesian Product wanted, set both DICTION_COLUMN and SOURCE_COLUMN to be -1

