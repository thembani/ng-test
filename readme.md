run: json-server --watch db.json


setup an angular router with the following pages:

1.  /artists
    -endpoint: http://localhost:3000/artists
    -method: GET
    --get the list of artists and display them on this page
    --allow the user to add, delete and edit existing artists
                --add -> will go to the /artist/add page ~ please see further instructions on this page below
                --delete -> will call the endpoint below to remove the artist
                            --endpoint: http://localhost:3000/artists/{artist.id}
                            --method: DELETE

                --edit -> will go to the /artist/edit/:id page ~ please see further instructions on this page below



2.  /artist/add
    -endpoint: http://localhost:3000/artists
    -method: POST
    -params: {
        "name":"",
        "details":"",
        "dateRegistered":"",
        "songs":[{
            "text":""
        }]
    }

    --build a form with validation that will post data to the API endpoint above


3.  /artist/edit/:id
    -endpoint: http://localhost:3000/artists/{artist.id}
    -method: "GET"
    --using the same form as /artist/add
            --get the artist details and prepopulate the form and allow users to edit the information.

    -endpoint: http://localhost:3000/artists/{artist.id}
    -method: PATCH
    -params: {
        "name":"",
        "details":"",
        "dateRegistered":"",
        "songs":[{
            "text":""
        }]
    }

    --using the same form as /artist/add
            --validate the form and update the artist's information using the above endpoint


4. Enhancements  
    - 