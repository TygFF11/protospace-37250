# README

prototypes
|  Column             |  Type        |  Option                          |
|  title              |  sring       |  null: false                     |
|  catch_copy         |  text        |  null: false                     |
|  concept            |  text        |  null: false                     |
|  user               |  references  |  null: false  foreign-key: true  |

belongs_to :user
has_many :comment


users
|  Column              |  Type       |  Option                          |
|  email               |  string     |  null: false                     |
|  encrypted_password  |  string     |  null: false                     |
|  name                |  string     |  null: false                     |
|  profile             |  text       |  null: false                     |
|  occupation          |  text       |  null: false                     |
|  position            |  text       |  null: false                     |

has_many :prototypes
has_many :comments


comments
|  Column               |  Type       |  Option                          | 
|  content              |  string     |  null: false                     |
|  prototype            |  string     |  null: false                     |
|  user                 |  reference  |  null: false  foreign_key: true  |

belongs_to :prototypes
belongs_to :user

