Indexed                Field	Description##
Id	                   Unique 18-character field that is system generated. This is the primary key for the object.
Name	                 Text-based field.
OwnerId	               Reference to the owner of the object.
CreatedDate	           Date and time when the record was created.
SystemModStamp	       Read-only field that contains the last date that the record was updated. This field is indexed where the similar LastModifiedDate is not, so consider using this one in your queries.
RecordType	           Id of the RecordType. RecordTypes are used to offer different UI results to certain users.
Master-Detail Fields	 Foreign key field used to indicate a master-detail relationship
Lookup Fields	Foreign  key field used to indicate a lookup relationship
Unique Fields	Custom   fields can be marked as unique when they are created, and this will automatically make them indexed.
External ID Fields	   Like unique fields, these custom fields can be marked as an External Id and are mainly used for integration purposes.
