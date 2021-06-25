# Classes

>JavaScript is a prototype-based language, meaning object properties and methods can be shared through generalized objects that have the ability to be cloned and extended. This is known as prototypical inheritance and differs from class inheritance.

In prototype-based language, objects can access to new methods from their prototypes even after they are created.

https://www.digitalocean.com/community/tutorials/understanding-prototypes-and-inheritance-in-javascript


Class example with _class_ keyword (ES6), constructors, inheritance, methods and getters:
```js
class HospitalEmployee {
  constructor(name) {
    this._name = name;
    this._remainingVacationDays = 20;
  }
  
  get name() {
    return this._name;
  }
  
  get remainingVacationDays() {
    return this._remainingVacationDays;
  }
  
  takeVacationDays(daysOff) {
    this._remainingVacationDays -= daysOff;
  }
}

class Nurse extends HospitalEmployee {
  constructor(name, certifications) {
    super(name);
    this._certifications = certifications;
  } 
  get certifications() {
    return this._certifications;
  }
  addCertification(newCertification) {
    this._certifications.push(newCertification);
  }
}

/* main */
const nurseOlynyk = new Nurse('Olynyk', ['Trauma','Pediatrics']);
nurseOlynyk.takeVacationDays(5);
console.log(nurseOlynyk.remainingVacationDays);
nurseOlynyk.addCertification('Genetics');
console.log(nurseOlynyk.certifications);
```