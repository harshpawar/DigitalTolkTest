Thank you for the code and giving me an opportunity to make spend some time to refector it.

I have studied the code for 15-20 mins.
let me share my view first.
- It is repository based structure of laravel application which is good for development and debug purpose.
- As I found the Application name is DTApi so application should return response in JSON format because response is used in APIs.
- I do not have the whole code so i don't know whether the code is done in response middleware or not so i did that.
- I also perform some of the code change in 3-4 functions. in BookingController file.
- I found in the code that in most of the functions error handling is not done so it is a fall back in the code.
- In the BookingRepository.php also there is no try catch block used so any error in the code results in the server error because no error handling.
- Directly use the helper functions inside the repository function is also a fall back because if a helper function array_except gives error by not getting expected keys in update function it will also generate server error.
- Laravel code base is too much old like 5.2 or 5.6 because array_except is depricated from 5.6 now in latest laravel Arr::expect($arr/$data,['key1','key2']) is used.

I have spent only 1 hour or 1 hour 30 min to study and refector some of the code not whole the code.
because found the same issue in all the functions. like error handling and all.
else structure wise the code is good.
- Also we can define authenticate user middleware to make less code in controller and repository.
- I found that some of the functions are used of old laravel version so i strongly recommand to use updated version of laravel and it's dependencies for the best performance.

Thank you and Regards
Harsh Pawar
mail: harsh.pawar.in@gmail.com
mobile: +91-9033327297