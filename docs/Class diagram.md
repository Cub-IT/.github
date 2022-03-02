```mermaid
classDiagram
    Participant o-- User
    Participant o-- Role
    Group o-- Participant
    Group o-- Post
    Post <|-- Apprisal
    Post <|-- GitAssigment

    class User {
        name : String
    }
    class Participant {
        user : User
        role : Role
        posts : Posts ???
    }
    class Role {
        <<enumeration>>
        OUNER
        ADMIN
        MEMBER
    }
    class Group {
        participants : List~Participant~
        posts : List~Post~
    }
    class Post {
        <<abstract>>
        creationDate
        modificationDate
        author : User
        title : String
        description : String
    }
    class Apprisal{

    }
    class GitAssigment {

    }
```
