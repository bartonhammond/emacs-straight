require("cloud/app.js");

Parse.Cloud.define("helloWorld", function (request, response) {
    response.success({message: "Hello world from Parse !"});
});


Parse.Cloud.define("helloWorld2", function (request, response) {
    var util = require("cloud/util.js");

    util.helloWorld(function (result) {
        response.success(result);
    });
});

Parse.Cloud.define("httpRequestExample", function (request, response) {
    Parse.Cloud.httpRequest({
        url    : "https://www.google.com",
        success: function (result) {
            response.success({message: "Request to google.com done !"});
        },
        error  : function (error) {
            console.log(error);
        }
    });
});


Parse.Cloud.job("testJOB", function (request, response) {
    console.log("Test job call success! ");
});

