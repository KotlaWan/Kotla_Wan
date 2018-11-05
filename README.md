function cloneObject(obj) {
    var clone = {};

    for(var i in obj) {
        if (typeof(obj[i]) != "object") {
            clone[i] = obj[i];
        }
        else {
            clone[i] = cloneObject(obj[i]);
        }
    }
    return clone;
}

var clone = cloneObject(personOriginal);
