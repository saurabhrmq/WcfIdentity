Unknown 0:13
Okay, so this is fine. Next, just a

Unknown 0:18
test result that if you want, we can like first start with this and

Unknown 0:26
correct. So template handle we will take it up later. Actually, first let's get test created and then we should see the output. That's the crux of the work, right? The template handle anyway we can get it later also not a problem actually. We can script the task stories accordingly. Then we can work on it accordingly. And then delete any we have not a problem. The here we need to have now we need to have an endpoint actually in the engine API. Current how we had evaluate right you aren't for a backtesting right one end point like that we need to have one end point for evaluate actually

Unknown 1:16
okay so same evaluate won't work

Unknown 1:22
same evaluate won't work means that expression has to be saved high dated. It should be part of the assembly. Then no need to work, right? But here there is one

Unknown 1:34
evaluate value here pass

Unknown 1:37
expression exactly. But the year here actually we have only evaluate where we are passing the expression also the current evaluated older

Unknown 1:50
one. Why that's all older one right?

Unknown 1:55
Yeah. What is fairness? Okay, once again, model puts. Okay, algorithm evaluate expression evaluate. Okay, algorithm

Unknown 2:41
table. He wants

Unknown 2:43
what we have ordered. There actually can you go to evaluate algorithm evaluate. Here, what is the payload we are passing it? Go to

Unknown 2:54
same for AI practice.

Unknown 2:57
Algo name, algo name, and then passing the RTX data and okay like this okay now I'm going name RTX data passing it right so similar RTX data only we need to form it similar to control application how it's forming it that way only we have to form it but that formation we should do based on the that input JSON from the table algo test table. For that we have to call model API, then get the test data from the input architect data. Put a point there. What that endpoint new endpoint supposed to

Unknown 3:43
do

Unknown 3:44
here our Hunter Engine API have to have a endpoint similar table. It we we have to have a new endpoint actually. But

Unknown 3:57
here we have this one also. Nah, here we can pass the expression and same input RTX data is getting passed and expression so this should work right.

Unknown 4:07
But in our case we will not pass this RTX data right? RTX data will be part of DB model itself. From UI I will just to the test only right? So that time I know only the test name and I'll say what is my test name, what is my algo name. That's all will be the important. Plus, yeah, actually expression whether I have to save it before running the test need not be right.

Unknown 4:39
Yeah.

Unknown 4:40
So that way, I should pass the expression also. You should not rely anything from the DB.

Unknown 4:53
Correct.

Unknown 4:54
So in that case, actually ports also needed. Actually, whatever okay ports in you when you evaluate the expression anyway will get the ports not a problem. So write it down clearly actually give a space line space because endpoint no yeah what this endpoint should accept as the input algo name name, comma test name, comma expression. Then the expression will take this test name from the DB. We can save it at import. Desk name. That's it. Because when you create a test thread, that time itself will be saving to the DB. Only expression expression also in that case will be saved to DB or expression need not be saved.

Unknown 6:08
No expression won't be saved right here. We have created a table.

Unknown 6:14
Yeah, test actually we have to save it actually. Okay, very first time we are creating algorithms, but expression even without saving the expression, I should be able to do the test actually. So that way, that's the reason we are expecting the expression in the input payload. Okay. So only this input is enough. Actually, I'll go name test name and expression. Okay. So now what we should do is that expression we are to we should not load it from the DLL actually assembly. One we should do that our endpoint how it's parsing it right. Same way we should parse the expression. expression at one end point which is accepting the expression as the input rate, similar to validate endpoint. That way, parse the expression. You have to get the assembly type reference. Okay. Then, what do you need? You need an input data. Probably write it next line. You need to get the input RTX data prepared similar to your console application. Further, how to input RTX data to be prepared? You have to call the model API get endpoint only to get the input JSON, all for the model API to get the input JSON for the given algorithm and the test name. Very first time when I create a new algorithm, right? That time anyway I have to save the algorithm. Without saving the algorithm, I cannot do the test. Okay, but once I have algorithm saved, I should be able to create a test and then save it and all. So that time without modifying, without saving, if if I make some changes to the expression, right? I may do only syntax check. Okay. After that, I will come and do the test here without saving to the TV, so that I can see how that outputs are looking like. Then I can save the changes of the expression actually. That's why we are going to accept the expression through payload itself to this endpoint evaluate endpoint. Okay, to get the input JSON to follow the given algorithm and to test name. Okay. Yes. Yeah. Okay. Now input RTX data is prepared. Now you have a expression from that expression. Get the type. Now you should be able to go through the same flow of run flow. Go back to the struggle with this input, input RTX data, not this one. Where is that? Algorithm evaluate, right? Whatever algorithm evaluate you are doing it right in the impact testing, right? Same code we should be able to leverage for the execution, you should leverage the same code. Not only that, we have to shift some of the logics from console application to this endpoint. Then you call this method internally. Service layer method internally.

Unknown 10:57
Okay.

Unknown 11:00
Okay. So for execute the test, we have to leverage the same code, whatever you have done in the A backtesting. Okay, same service layer method, and then the console application. Some logics may be there, right? To read the input JSON. After that, we may be doing something right. That something is has to be moved to the same pointer. Okay. Whatever we are doing with input JSON preparation, right? That input JSON preparation itself, from that input JSON preparation only, whatever we do batching and then executing and all right, that logic will shift it to this endpoint.

Unknown 11:58
Okay. Now we have to store that test result somewhere, right? Results

Unknown 12:08
really needed, or we'll just give the response. Okay. Now the results, whatever we returned in the A backtesting, right? Whether the same result is good enough to trend it here.

Unknown 12:23
That I have to check it

Unknown 12:28
once. Actually, you have input the data that are text data. We can send the RTX data response so that you get an array here. Output is also whatever the they are actually what we did. We returned all the variables, right?

Unknown 12:45
Only Spark, right?

Unknown 12:48
Output variables. Exactly touch the point. Okay, wherever we are doing that Spark alone, we are returning to the caller, right? That Spark filter alone not needed. Whatever the output comes after executing all the internal batches, right? Let's say two hours batches or four hour batches is what we splitted and executed in the console application, right? After executing all the batches, then we used to return the data, right? Output data, right? That output data we filtered only for Spark, but here in this case we will not filter it. Actually, we will return all the output data. Okay. That way, what we can do is we will have one input. What our Excel is having as a input data, that also we will return it. Then output also let's return in the response actually in the in that particular endpoint. Asian RTX data series, RTX data list of RTX data we can return actually the endpoint. Now that list of RTX data endpoint whether you want written the same way or little better way for UA purpose like with the time series time series value and all we can do that instead of RTX data.

Unknown 14:12
Yeah, we need that somewhere it should be stored because if six tests are running and someone wants to check fourth test.

Unknown 14:22
Ah, check correct. Otherwise, every time whenever you expand it, you have to keep running it. That will be too costly. Right? That's what you wanted to see the result getting stored whenever we run it. Actually,

Unknown 14:38
yeah. So somewhere in here only we can store the result also because we have everything

Unknown 14:44
correct. Then when we go to the EI, we'll store it, then return it. Then after test execution, it has to call this method. Then the above endpoint will not return it. Always will just store it in the div instead of returning it. Yeah, run test. We had some button, right? Yes. Suppose if we'll add

Unknown 15:19
test. Don't have the edit.

Unknown 15:27
Yeah, that is best actually. So whenever you run the test, right? Create test. Yeah, not this one. Even that individual test also. What you do? You have a method. Any post method is there? No. So in the post method, we should be able to, or we can add a put actually in the model APA, so that output alone. Whenever I run it, I should be able to update only the result JSON alone actually. Okay. Put operation only for the result generation actually. Then the get endpoint always you get written the everything actually. Including both input and output also, and then yeah, that line you should not return it actually from this API. Instead, this itself will call the model API, then save the result actually.

Unknown 16:43
List of our text data, but it should be in the graph format, whichever is the required

Unknown 16:49
format. Correct. Required format. We will save it. Then what you will do? You anyway will you retrieving it? Right? You have get in point. Get all algo test by algo name and test name right. So as part of that, anyway you get both input JSON and output JSON also for all the test. So that whenever you expand it, right, it will be just immediately you can plot it actually without a delay. Okay, only whenever people are running the test, that time only the Avo API endpoint will be called actually. Called correct. That endpoint whenever it comes, it will save the output also to the DB actually test test entity. So what I suggest better have one confidence based with the flow diagram. Actually, okay. From UA we are making three AP calls. One is for bulk config, one for modern APA, and some endpoint in the engine APA. Right. So this flow from test flow alone. Okay, not anything else. Only test flow alone. First, where are we making it? Whenever you create a test, where the endpoints are getting called? Okay, after that, whenever I do run test, which endpoint is getting called? Like that, just flow alone you put it, and then for each flow, then whatever you put in the notes here, right? That notes also come to that page actually. Saying that model API, this one has to endpoint has to be there. Bulk config API, this endpoint has to be there. Engine API, this endpoint has to be there. Total three APIs we need to add the endpoints. n points only thing is that interaction alone just so it is not diagram so that it will be clearly evident clearly understandable actually correct okay so
