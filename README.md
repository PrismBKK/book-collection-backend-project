## book-collection-backend-project

    User register:
        endpoint:/auth/register
        HTTP method: POST
        require body:{
            firstName:string,
            lastName:string,
            email:string,
            username:string,
            password:string
        }
        Response(Success):
        {
            message : "User has been created successfully",
            status: 200
        }
        Response(Failure):
            Missind Data :
            {
                message: "Server could not register there are missing data from client",
                status:400
            }
            Database Connection Error:
            {
                message: "Server could not register because database connection",
                status:500
            }

    User login:
        endpoint:/auth/login
        HTTP method: POST
        require body:{
            username:string,
            password:string
            }
        Response(success):
        {
            message: "login successfully"
            ,token,
            status:200

        }
        Response(Failure):
            Password not valid:
            {
                message: "password not valid",
                status: 401
            }
            User not found:
            {
                message: "user not found",
                status: 401
            }
            Database Connection Error:
            {
                message: "Server could not login because database connection",
                status:500
            }


    Create book:
        endpoint:/book/create
        HTTP method: POST
        require body:
        {
            book_name:string,
            auth_name:string,
            published_year:string,
            publication_time:int,
            categoly:string,
        }
        Response(Success):
        {
            message : "Books has been created successfully",
            status: 200
        }
        Response(Failure):
            Missind Data :
            {
                message: "Server could not register there are missing data from client",
                status:400
            }
            Database Connection Error:
            {
                message: "Server could not register because database connection",
                status:500
            }


    Update book:
        endpoint:/book/:bookId
        HTTP method: PUT
        require body:
        {
            book_name:string,
            auth_name:string,
            published_year:string,
            publication_time:int,
            categoly:string,
        }
        Response(Success):
        {
            message : "Books has been update successfully",
            status: 200
        }
        Response(Failure):
            Missind Data :
            {
                message: "Server could not update there are missing data from client",
                status:400
            }
            Database Connection Error:
            {
                message: "Server could not update because database connection",
                status:500
            }


    Delete book:
        endpoint:/book/:bookId
        HTTP method: DELETE
        Response(Success):
        {
            message : "Books has been delete successfully",
            status: 200
        }
        Response(Failure):
            Missind Data :
            {
                message: "Server could not delete there are missing data from client",
                status:400
            }
            Database Connection Error:
            {
                message: "Server could not delete because database connection",
                status:500
            }



    Add book to collection
        endpoint:/add_collection/:username
        HTTP method: POST
        require body:
        {
            book_id:int,
        }
        Response(Success):
        {
            message : "Books has been add collection  successfully",
            status: 200
        }
        Response(Failure):
            Missind Data :
            {
                message: "Server could not add collection  there are missing data from client",
                status:400
            }
            Database Connection Error:
            {
                message: "Server could not add collection because database connection",
                status:500
            }


    Call book collection
        endpoint:/collection/:username
        HTTP method: GET
        Response(Success):
        {
            collection: [bookname1,bookname2,bookname3,......],
            status: 200
        }
        Response(Failure):
            Missind Data :
            {
                message: "Server could not call book collection  there are missing data from client",
                status:400
            }
            Database Connection Error:
            {
                message: "Server could not call book collection because database connection",
                status:500
            }
