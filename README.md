Unknown 0:02
Test test entity. So what I suggest better have one conference page with the flow diagram. Actually, okay. From UA we are making three AP calls. One is for bulk country, one for model APA, and some endpoint in the engine API, right? So this flow from your test flow alone, okay, not anything else. Only test flow alone. First, where are we making it? Whenever we create a test, where the endpoints are getting called? Okay. After that, whenever I do run test, which endpoint is getting called like that? Just to flow along, you put it, and then for each flow, then whatever you put in the notes here, right? The notes also you copy to that page actually, saying that model API this one has to endpoint has to be there. Bulk config API, this endpoint has to be there. Engine API, this endpoint has to be there. Totally three APAs. We need to add the endpoints. Only thing is that interaction alone. Just show it in a diagram so that it will be clearly evident and clearly understandable. Actually,

Unknown 1:15
correct.

Unknown 1:17
Okay. So for that now we have to announce model APA with one entity, all these endpoints, and then bulk config API to parse the Excel and then save it here. Then engine APA one evaluate endpoint which accept these parameters actually, right? With the expression and the test name and all. Okay, so now go back to the yeah. So now run all test means anyway we can call that we can make that many calls, okay. So whenever you click run all test, anyway you know all the tested. You just you can trigger each one of them, and then you can see. Now with this actually for top we are showing five successful, one failed actually. Okay, we are showing some status here. This one actually we need to have something status in the test table only. Actually, a cell status whether particular test is successful or failed. That's it. Successful or failed status. So that whenever try is that we can see the count. How many are successful? Count is so successful. How many failed? You saw failed. But how to identify successful and failed criteria is the next question. Yes. Right. So as long as it executes, that's not the root test actually. Test is if I say input data is so and so, then what is the output data expected? That should be there. Then only it's a proper test assertion actually. Right? Can you go back to Excel sheet? Now we can have one more rock set. You can say expected output. This also I can say what is expected output for my test case. This is no longer just an input. This also input data means it is having expected output also. Okay, so expected output can be telemetry data. Go to telemetry data. Put that same schema here. Then for what timestamp, what value I am expecting it? Probably we need to put the variable name under similar to there. Actually, what we had, we had a one variable called spark, right? So put the spark. Remove the column B C column remove the B C D E now for this time system what is per duration has to come minus one zero or some value has to come that we will see actually based on whatever is coming in your test case, right? After filling this, then accordingly you put it in the expected output such a way that it will pass. Okay, one is just about 100 actually have zero 100 anything is fine. Now what we can do that endpoint one is it's storing the output along with that it can do this comparison actually whether that required output variable like Spark whether I have this timestamp value matched before calling the model API yeah to the output. assessment check. Then decide successful or failed. Then the below table, right? Add one more field after result. JSON status actually test run status. By default, it can be empty. Okay, you can accept the nullable fail so that only when it runs, you will come to know successful or failed. Very first time, let it be null luxury. Or we can have not nullable, and then very first time we can say not executed or something like that. Okay, not executed. executed as a first step, very first time.

Unknown 6:28
Okay. Then the

Unknown 6:32
UA also just not need not just so only successful and filmed. We can have one more count called not executed count also in the even though the DX it doesn't show we can have one more status not executed successful failed and not executed so far like that okay yeah right okay so. so that way the algo test pro will look good. Okay, what else? Any anything else in the UX? Only thing is export dot x. Export is whatever that output is there. No, that you wanted to export here. Actually, I say Excel format. This trend actually whatever is trending right, so that should have both input and output actually. So output also I want to export it as an Excel, not expected output, actual output. That output JSON result that JSON whatever you are storing it right. That result that JSON if you want to export, or this can be done in the claim serial. Yeah,

Unknown 8:15
if we have the details here, right? It's the result JSON and the test runs. Correct. Sorry, result. We can.

Unknown 8:27
Yeah, only from test to result only. Test result JSON only. We should get it actually. For that also, let's have one endpoint similar to that input file. How are we downloading it through? download right here, algo test input we are downloading same way add on endpoint download for algo test output. Ultimately, engineer B will not deal with any Excel sheet. Bulk cut because we are going to put the this Excel download, Excel upload, and done. Okay, from the model IP that results.

Unknown 9:31
Okay, fine. Okay,

Unknown 9:34
so this is covered. What else is there not covered in the X? It says last and successfully at so on show time. We don't have a time. Stand. And then add it. Add it up to this date. Okay. I understand. can say run timestamp. Just prefix with run timestamp. Yeah, that's fine. Very first time we should not put anything actually.

Unknown 10:28
Hmm.

Unknown 10:30
Okay. Correct. Fine. Go back to EX. Anything else we left? Exporter here, and we'll call that same input. Then we'll bind it and then show it here. Any other API requirement tree here? No. No. No. Okay. Good. So now with this, actually, you also load fast with this design approach. You don't need to run every time, right? Whenever you come here, it will run fast. Actually, whenever you hit the rear, also it will run. Then it can call the other endpoint just to refresh it. Actually,

Unknown 11:33
okay.

Unknown 11:36
Anything else not here?

Unknown 11:40
So that's it about this.

Unknown 11:43
Probably what you do is probably explain the model EPA alone to saurab now, and then let him started. Meanwhile, you can put the flow under this one under, and then probably sometime tomorrow you can sell the details. Actually, not a problem. Okay, so the replication get started with this. Okay, okay. We'll close now. Yeah, and just one small thing. Sure.

This transcript was generated by https://otter.ai
