```
    urther Reading

Django Rest Api application Overview

We will build a Django Rest Apis Application that can create, retrieve, update, delete and find Tutorials by title or published status.

The following table shows overview of the Rest APIs that will be exported:
Methods	Urls	Actions
GET	api/tutorials	get all Tutorials
GET	api/tutorials/:id	get Tutorial by id
POST	api/tutorials	add new Tutorial
PUT	api/tutorials/:id	update Tutorial by id
DELETE	api/tutorials/:id	remove Tutorial by id
DELETE	api/tutorials	remove all Tutorials
GET	api/tutorials/published	find all published Tutorials
GET	api/tutorials?title=[kw]	find all Tutorials which title contains 'kw'

And the code for API Views will look like this-

@api_view(['GET', 'POST', 'DELETE'])
def tutorial_list(request):
    # GET list of tutorials, POST a new tutorial, DELETE all tutorials
 
 
@api_view(['GET', 'PUT', 'DELETE'])
def tutorial_detail(request, pk):
    # find tutorial by pk (id) 
    # GET / PUT / DELETE tutorial
    
        
@api_view(['GET'])
def tutorial_list_published(request):
    # GET all published tutorials
```