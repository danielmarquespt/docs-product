# Possible Data Loss Warning

Message : `The [parameter_name] parameter in SAP is of [parameter_type] type, and is mapped to Decimal. This can result in data loss. Review if your data fits into the boundaries of the Decimal data type`

Cause : The parameter mentioned in the warning can have values that are out of the range of the Decimal data type of OutSystems. As the parameter is currently mapped to Decimal, this can lead to the following behavior:

* If the remote function receives a value lower than -296+1, or higher than 296-1, you receive an error message at runtime.
* If the received value is longer than the number of digits that the system supports, it will be rounded to the maximum length.

Recommendation : Check if your SAP data contains values that lead to the above situations. To avoid them, you can use Text data type instead of Decimal.

