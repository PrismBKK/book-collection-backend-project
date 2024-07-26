# book-collection-backend-project
Backend
    User register:
        HTTP method: POST
        requirement body:firstName,lastName,email,username,password
        endpoint:/auth/register

    User login:
        HTTP method: POST
        requirement body:username,password
    endpoint:/auth/login

    Create book:
        HTTP method: POST
        requirement body:book_name,auth_name,published_year,publication_time
        endpoint:/book/create

    Update book:
        HTTP method: PUT
        requirement body:book_name,auth_name,published_year,publication_time(as you want to edit)
        endpoint:/book/:bookId

    Delete book:
        HTTP method: DELETE
        endpoint:/book/:bookId

    Add book to collection
        HTTP method: POST
        requirement body:book_id
        endpoint:/add_collection/:username

    Call book collection
        HTTP method: GET
        endpoint:/collection/:username

