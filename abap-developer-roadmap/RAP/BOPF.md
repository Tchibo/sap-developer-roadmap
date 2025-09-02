#Advanced 

> [!todo] I wonder whether BOPF should be a subtopic
> Explaining BOPF as the precursor for RAP and the modelling patterns it added might be worth a shorter text without io_modify detail. Or even include this in subtopic 'Business Objects' and drop BOPF alltogether.

The Business Object Processing Framework (**BOPF**) is an older SAP framework that is now in maintenance mode and should be avoided for new development projects. However, understanding BOPF is important because it laid the foundation for modern RAP development.

BOPF's main contribution was introducing the concept of **business objects** to ABAP development. A business object in BOPF is a structured container that groups related business data together with its operations. These business objects are organized in hierarchical structures, meaning they can have parent-child relationships between different data entities.

BOPF business objects include several key components: automatically generated Create, Update, and Delete (CUD) operations accessible through the io_modify interface, associations that define relationships between different entities, validations to ensure data integrity, and determinations that automatically calculate or derive field values.

While BOPF established these fundamental concepts that developers still use today, implementing solutions in BOPF requires significantly more coding steps and configuration compared to its successor. RAP has replaced BOPF as the preferred framework because it simplifies the development process while providing the same business object concepts in a more modern, cloud-ready architecture.

### Resources
> [!todo] Text for Link
> Please provide the text for the link you'd like to see in the roadmap

#article https://blog.sap-press.com/abap-restful-application-programming-model-versus-bopf