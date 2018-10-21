# dotNETImageHosting

TODO:

- [ ] Create a database.

<details> 
    <summary>Database structure</summary>
        <br>
        <details>
            <summary> Users</summary>

                Users : {
                    nID, // primary key
                    strDisplayName,
                    strEmail,
                    nPasswordHash,
                    nUserLevel
                }

</details>
        <details>
            <summary>UserImages</summary>

                UserImages : {
                    nID, // primary key
                    nUserID, // foreign key
                    nUniqueImageID, // foreign key
                    nCreationDateMiliseconds
                }

</details>
        <details>
            <summary>UniqueImages</summary>

                 UniqueImages : {
                    nID, // primary key
                    nHash,
                }

</details>
        <details>
            <summary>Tags</summary>

               Tags : {
                    nID, // primary key
                    strTagName
                }

</details>
        <details>
            <summary>TagImages</summary>

               TagImages : {
                    nID, // primary key
                    nTagID, // foreign key
                    nImageID // foreign key
                }

</details>
        <details>
            <summary>Likes</summary>

                Likes : {
                    nID, // primary key
                    nImageID, // foreign key
                    nUserID, // foreign key unique
                    bIsDislike,
                    nCreationDateMiliseconds
                }

</details>
        <details>
            <summary>Comments</summary>

                Comments : {
                    nID, // primary key
                    nImageID, // foreign key
                    nUserID, // foreign key
                    strContent,
                    nCreationDateMiliseconds
                }

</details>
</details>
