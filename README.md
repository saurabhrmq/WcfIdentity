Yeah. So now you have a list of text and then description and then Excel content there. If you want to edit it, you can go and edit it. As part of post, we should be able to even save the content actually, right? Whenever you upload it, like that. So now this flow is clear, right? Basically creating the test under. Then download template. Let's come to the download template. The download template is nothing but the the

Unknown 0:46
action sheet whatever you prepared, right?

Unknown 0:49
Okay.

Unknown 0:51
That is the both are same only, right? Download template, download input. Download input is whatever the input I prepared and uploaded earlier for the test that same file only I wanted downloaded.

Unknown 1:05
That's the this was important.

Unknown 1:13
Not that way. Whatever you prepared here, this is one of the test case input. Let's say test six input. That's what you prepare now. That you will be uploading it, or if you want to download it, you can use the download input option actually.

Unknown 1:30
Okay. Okay. If you go to edit, then you can do upload actually.

Unknown 1:35
Okay.

Unknown 1:36
What is the download template means? What are the Excel sheet you have?

Unknown 1:41
You have to give that schema without the data.

Unknown 1:48
Okay. Otherwise, how user will know that how to fill that vexel?

Unknown 1:53
Then we have to document somewhere else, right? Yeah. So there's the timestamp and all the things and all the constant will. with no values. Correct. That's what we wanted to get in the template. Actually, for the given model, anyway we know the input outputs, right?

Unknown 2:14
Now input outputs you leave it. Only inputs alone will take it. Not even input output.

Unknown 2:22
Okay, input output also we have to consider not only just

Unknown 2:29
okay that very first input output and not needed only input alone we have to consider good input output step

Unknown 2:40
input output step this

Unknown 2:42
one. Yeah, here we need to consider only the inputs actually.

Unknown 2:47
Okay, in this case, fan split set point is the only input.

Unknown 3:01
Hmm.

Unknown 3:03
This is for template option. Template option, you consider only the input where if it's having a something array array right, then array means it's a time series data double array.

Unknown 3:18
Okay, if anything like a primitive type, like a string or double or float, then it's a constant actually.

Unknown 3:35
Double array collection, float, float, double array collection, float, double array.

Unknown 3:41
So double array collection only should be the time series.

Unknown 3:46
Not collection actually double array.

Unknown 3:50
Okay. Okay, double array collection also is a time series only, but actually that collection I'm thinking how to avoid actually the collection.

Unknown 4:04
Okay.

Unknown 4:06
Actually, in that case, we need to have some more thing. Actually, okay. Only that farmer we need to take it. Actually, have starting with that variable name or collection some form we have to introduce. Okay, collection we will discuss probably sometime tomorrow.

Unknown 4:29
Okay, so double array we have to put it into time series data.

Unknown 4:36
Double array string array should go to time series data, where this download template API will go here only, right? Download template API.

Unknown 4:48
Or else we can prepare a job based on

Unknown 4:54
the UAE. No, no, not in the UAX. We should better to be in the API only, so that you will be lightweight actually. So the download template actually for this test actually we will go to engine AP only.

Unknown 5:12
Okay. For testing purpose, test flow. So there only you will keep the download template also.

Unknown 5:21
Okay.

Unknown 5:23
Okay, that's the engine API. Engine API have endpoint to download the template.

Unknown 5:31
How it can download time series data sheet should contain the double array and the string array data type of input.

Unknown 5:40
Okay.

Unknown 5:49
Should should should be

Unknown 5:54
for for double array and string array.

Unknown 6:03
Okay.

Unknown 6:06
Okay. For constant data should be for double string.

Unknown 6:17
What are the other primitive types? Not other than array, that way we want to put it actually.

Unknown 6:25
Float integer.

Unknown 6:27
Yes, float integer byte whatever comes right without array and collection. Without an array of a collection. Without array and collection, put it into constant.

Unknown 6:43
Whatever comes without array under collection flag, it should go to constant data.

Unknown 6:51
Okay.

Unknown 6:52
Okay. So that's how we have to prepare these things, and only data alone will keep it empty. User can fill it. Okay. That's how we will provide the template.

Unknown 7:04
Okay, sure.

Unknown 7:08
Okay, so this is fine. Next,

Unknown 7:12
just the test result that if you want, can like first start with this and correct. So template random. We will take it up later. Actually, first
[This note may be incomplete because it was exported before processing was finished.]
