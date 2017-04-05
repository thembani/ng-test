##### NOTE: Please make sure you have [node installed](https://nodejs.org/en/)
****

##### install json-server
    - Open command line in the ng-test folder and run "npm install json-server -g"
##### install lite-server
    - Open command line in the ng-test folder and run "npm install lite-server -g"
____
##### run: json-server --watch db.json
##### run: lite-server
____

##### setup an angular router with the following pages:
____

###### 1.  /artists
    - endpoint: http://localhost:3000/artists
    - method: GET
        - get the list of artists and display them on this page
        - allow the user to add, delete and edit existing artists
        - add -> will go to the /artist/add page ~ please see further instructions on this page below
        - delete -> will call the endpoint below to remove the artist
            - endpoint: http://localhost:3000/artists/{artist.id}
            - method: DELETE
            - edit -> will go to the /artist/edit/:id page ~ please see further instructions on this page below



###### 2.  /artist/add
    - endpoint: http://localhost:3000/artists
    - method: POST
    - params: {
        "name":"",
        "details":"",
        "dateRegistered":"",
        "songs":[{
            "text":""
        }]
    }
    - build a form with validation that will post data to the API endpoint above


###### 3.  /artist/edit/:id
    - endpoint: http://localhost:3000/artists/{artist.id}
    - method: "GET"
    - using the same form as /artist/add
        -get the artist details and prepopulate the form and allow users to edit the information.
    - endpoint: http://localhost:3000/artists/{artist.id}
    - method: PATCH
    - params: {
        "name":"",
        "details":"",
        "dateRegistered":"",
        "songs":[{
            "text":""
        }]
    }
    -using the same form as /artist/add
        -validate the form and update the artist's information using the above endpoint