# Team Members

- Simon Asenime, Christian Gould, Kas Taghavi, Muhammad Ashraf

# For Thought

## 1. Is The current method of saving the classifier blocking to the tornado IOLoop? Justify your response.

- The current method is currently blocking tornado as the load\_model function in turicreate is a synchronous blocking call. To fix this we should write a wrapper function to load the model asynchronously.

## 2. Would the models saved on one server be usable by another server if we migrated the saved documents in MongoDB? Justify your response.

- The models should be usable by another server as the models are in a format that turicreate understands so if the other server is using turicreate the models should work just fine. Otherwise we would need to export them to another format.
