
### Contributors : Thefr33radical, Mahendra
# Script to convert nested json object to dictonary
# Script to convert nested json object to Dataframe
# Script to convert nested json object to CSV

********************************************************************************

## Notes

Better optimized version using generators will be published soon.
Result JSON OBJECT to CSV or DATAFRAME can be converted in one more step.
 1. Remove commented lines to load key value pairs into dictionary obj
 2. Use pandas library to convert dictionary to dataframe
 3. Convert Datframe to CSV


********************************************************************************
## ALGORITHM to Extract (key,val) pair in a nested JSON_OBJECT:

1. call EXTRACT(key,val)
2. if val type equals JSON_ARRAY
    1. for i in JSON_ARRAY
        1. call EXTRACT(i,val[i])
    2. return
3. if val type equals JSON_OBJECT
    1. for i in  JSON_OBJECT.KEYS()
        1. call EXTRACT(i,val[i])
    2. return
4. if val type equals STRING
    1. print val

**********************************************************************************
