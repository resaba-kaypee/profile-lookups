# profile-lookups

//Setup
var contacts = [
    {
        "firstName": "Akira",
        "lastName": "Laine",
        "number": "0543236543",
        "likes": ["Pizza", "Coding", "Brownie Points"]
    },
    {
        "firstName": "Harry",
        "lastName": "Potter",
        "number": "0994372684",
        "likes": ["Hogwarts", "Magic", "Hagrid"]
    },
    {
        "firstName": "Sherlock",
        "lastName": "Holmes",
        "number": "0487345643",
        "likes": ["Intriguing Cases", "Violin"]
    },
    {
        "firstName": "Kristian",
        "lastName": "Vos",
        "number": "unknown",
        "likes": ["JavaScript", "Gaming", "Foxes"]
    }
];


function lookUpProfile(name, prop){
// Only change code below this line
    for(let i = 0; i < contacts.length; i++){
        if(name === contacts[i].firstName){
            if(contacts[i].hasOwnProperty(prop)){
                return contacts[i][prop];
            } else {
                return "No such property";
            }
        }
    } return "No such contact";
}

// Change these values to test your function
lookUpProfile("Akira", "likes");

"Kristian", "lastName" should return "Vos"
Passed
"Sherlock", "likes" should return ["Intriguing Cases", "Violin"]
Passed
"Harry","likes" should return an array
Passed
"Bob", "number" should return "No such contact"
Passed
"Bob", "potato" should return "No such contact"
Passed
"Akira", "address" should return "No such property"
