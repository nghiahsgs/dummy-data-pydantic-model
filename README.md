# dummy-data-pydantic-model
dummy data pydantic model

```python
from pydantic_factories import ModelFactory
from pydantic import BaseModel

class User(BaseModel):
    id   : str
    name : str
    age  : int


# user1 = User(
#     id = '001',
#     name = 'name',
#     age = 20
# )

class UserFactory(ModelFactory):
    __model__ = User

users = UserFactory.batch(3)
print(users)
users = [e.dict() for e in users]
print(users)
```
