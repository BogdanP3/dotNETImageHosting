# dotNETImageHosting

TODO:


<details> 
  <summary>Create a database.</summary>

    <details>
        <summary>Users Table</summary>
        Users : {
            nID, // primary key
            strDisplayName,
            strEmail,
            nPasswordHash,
            nUserLevel
        }
    </details>


    UserImages : {
        nID, // primary key
        nUserID, // foreign key
        nUniqueImageID, // foreign key
        nCreationDateMiliseconds
    }


    UniqueImages : {
        nID, // primary key
        nHash,
    }


    Tags : {
        nID, // primary key
        strTagName
    }


    TagImages : {
        nID, // primary key
        nTagID, // foreign key
        nImageID // foreign key
    }


    Likes : {
        nID, // primary key
        nImageID, // foreign key
        nUserID, // foreign key unique
        bIsDislike,
        nCreationDateMiliseconds
    }


    Comments : {
        nID, // primary key
        nImageID, // foreign key
        nUserID, // foreign key
        strContent,
        nCreationDateMiliseconds
    }

</details>
