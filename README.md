# dotNETImageHosting

TODO:


** DB
```
Users : {
    nID, // primary key
    strDisplayName,
    strEmail,
    nPasswordHash,
    nUserLevel
}
```

```
UserImages : {
    nID, // primary key
    nUserID, // foreign key
    nUniqueImageID, // foreign key
    nCreationDateMiliseconds
}
```


```
UniqueImages : {
    nID, // primary key
    nHash,
    strDiskLocation
}
```


```
Tags : {
    nID, // primary key
    strTagName
}
```


```
TagImages : {
    nID, // primary key
    nTagID, // foreign key
    nImageID // foreign key
}
```


```
Likes : {
    nID, // primary key
    nImageID, // foreign key
    nUserID, // foreign key unique
    bIsDislike,
    nCreationDateMiliseconds
}
```


```
Comments : {
    nID, // primary key
    nImageID, // foreign key
    nUserID, // foreign key
    strContent,
    nCreationDateMiliseconds
}
```