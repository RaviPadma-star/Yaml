# Yaml
This is about yaml
yaml- yet another markup langauage
yaml - yet another markup language 

yaml -> is data format used to exchange data! it is similar to xml and json file used to store data
- in yaml we can store only data but not commands
- it is kown as data seriailsation!
Data Serialisation: -> is convert to object to file, and then file to convert to object is known as De-serailisation
    -- Configuration files -> Docker, Kubernates etc 
    -- Logs, Caches
    
    Benifits of yaml:
    --Simple and easy to read, 
    -- it has a strict syntax, -- indendation is important
    -- Easily to convertable for ex : json, xml
    -- Most lang used as yaml
    -- more poerfull when respresnting comlex data
    -- parser, etc various tools avialbale
    -- Prsing is easy read to easy
    
    -- in yaml if we put --- its makes has Each document start from 0 to more
    -- if we want end a document in yaml use ...
    
"apple" : "I am a  red fruit"
2 : "its a value"
---
#lists yaml are case sensitive, Spaces are imp and blocks imp
- apple
- mando
- banana
- Apple

---
cities : 
 - new delhi
 - hyderabad
 - telenagana
 
 ---
 {"mango" : "yellow fruit", age: 36}

 ...
 
 students: !!seq
  - marks
  - roll_no
  - name

#like this also
cities : [new Delhi, mumbai]

# some of the key of the sequence will be empty
# spare sequence

spare seq:
 - hey
 - how
 -
 - Null
 - sup

# nested sequence:
-
 - mango
 - banana
 - carrot
-
 - bats
 - balls
 - spiner
-
 - shoot

 #example
 [
    [
        "mango",
        "banana",
        "carrot"
    ],
    [
        "bats",
        "balls",
        "spiner"
    ],
    [
        "shoot"
    ]
]

# key : values pairs are called maps
!!map

#nested mapping map within map
name: padmaravi
role:
 age: 89
 student: sfnnas

role: {age: 89, student: sfnnf}

# pairs: keys may have duplicate values
# !!pairs
pair ex: !!pairs
 - job: student
 - job: teacher
 #this will be a has table contaiing arrays
pair ex: !!pairs [job: student, job: teacher]

# !!set will allow  you have to Unique Values
names: !!set
  ? Ravi
  ? Padma
  ? udayabhanu

# Dictionary !!omap

People: !!omap
 -Kunal:
    name: Kunal Kushwawa
    age: 46
    height: 15.5
 -Rahul:
    name: RAhul op
    age:544
    height: 16546

# Resuing proprties using achors

liking: &likes
  dislike: mango
  fav fruits: grapes

person1:
    name: Ravi
    <<: *likes

person2:
    name: RaviPadma
    <<: *likes

person3:
    name: Ravi Udayabhanu
    <<: *likes
    dislike: berries
 
 
 Yaml file:
 ---
school:
- nameofschool: dps
  principal: Ravi
  students:
  - rno: 12
    name: PAdma Ravi
    marks: 94
    
    
 
Json file:
{
    "school": [
        {
            "nameofschool": "dps",
            "principal": "Ravi",

            "students" : [
                {
                    "rno": 12,
                    "name": "PAdma Ravi",
                    "marks": 94
                }
            ]
        }
    ]
}


➡️ Resources:
Lens: https://k8slens.dev/?utm_source=Cloud...
Monokle: https://github.com/kubeshop/monokle?u... 
Datree: https://datree.io/?utm_source=youtube...
How to validate Kubernetes YAML files: https://itnext.io/how-to-validate-kub...

