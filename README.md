- 👋 Hi, I’m @theguvnors
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
theguvnors/theguvnors is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->


([(\w+\?\.)]+[\s+](!==\s+))(undefined)(\s+\&&\s+)([(\w+\?\.)]+[\s+](!==\s+))(null)


console.clear();
let x = [{a:1,b:2},{a:10,b:2},{a:11,b:2}]
let first = x.map(m => {return m.a})

let y = [{a:1}, {a:3}, {a:2}];
let y1 = [{a:1}, {a:3}];
let z = [{a:1}, {a:10}, {a:11}];
let z1 = [{a:11}, {a:10}, {a:11}];




function optionMatcher(firstItem: any[], OtherItems: any[]){

    let uniqueItems = [...new Set(OtherItems.map(x => {return x.a}).sort())];
    let uniqueFirstItems = [...new Set(firstItem.sort())];

    return Array.isArray(uniqueItems) &&
        Array.isArray(uniqueFirstItems) &&
        uniqueItems.length === uniqueFirstItems.length &&
        uniqueItems.every((val, index) => val === uniqueFirstItems[index])
}

console.log(optionMatcher(first, y)); // false
console.log(optionMatcher(first, y1)); // false
console.log(optionMatcher(first, z)); // true
console.log(optionMatcher(first, z1)); // false
