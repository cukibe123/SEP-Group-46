# Report for Assignment 1

## Project chosen

Name: video.js

URL: https://github.com/videojs/video.js

Number of lines of code and the tool used to count it: 68299

Programming language: JavaScript

## Coverage measurement

### Existing tool
The existing coverage tool that we use for this project is Istanbul. The coverage of this tool has already been implemented in the project and what we have to do is to enable the coverage tool on.

After digging around and getting some basic knowledge and intuition about the project, we figured out the way to enable the test procedure to return the coverage report under the HTML format:

In both rollup.config.js and karma.conf.js files:

This is the initial value of const CI_TEST_TYPE:
![Description of the image](https://github.com/thinhrick0101/demo/blob/main/t%E1%BA%A3i%20xu%E1%BB%91ng%20(1).jpeg)
![Description of the image](https://github.com/thinhrick0101/demo/blob/main/t%E1%BA%A3i%20xu%E1%BB%91ng.jpeg)

In order to enable the report coverage to be returned, we change the value of this constant into the string: ‘coverage’
![Description of the image](https://github.com/thinhrick0101/demo/blob/main/t%E1%BA%A3i%20xu%E1%BB%91ng%20(2).jpeg)
![Description of the image](https://github.com/thinhrick0101/demo/blob/main/t%E1%BA%A3i%20xu%E1%BB%91ng%20(3).jpeg)

After reassigning new value to the const CI_TEST_TYPE, we can simply run the command: 
![Description of the image](https://github.com/thinhrick0101/demo/blob/main/t%E1%BA%A3i%20xu%E1%BB%91ng%20(4).jpeg)


This command starts cleaning all already built folders, then it lints all the source/test files to ensure conventions are maintained. Accordingly, the build of the system runs and all test units are executed.  

This is the coverage report that we received after running all unit tests.
![Description of the image](https://github.com/thinhrick0101/demo/blob/main/t%E1%BA%A3i%20xu%E1%BB%91ng%20(5).jpeg)

### Your own coverage tool

** Nguyen Duc Thinh
### Your own coverage tool
Function 1: textContent() function in src/js/utils/dom.js

The original code:

![Description of the image](https://github.com/thinhrick0101/demo/blob/main/t%E1%BA%A3i%20xu%E1%BB%91ng%20(6).jpeg)

The instrument code:

![Description of the image](https://github.com/thinhrick0101/demo/blob/main/t%E1%BA%A3i%20xu%E1%BB%91ng%20(7).jpeg)

My coverage tool and existing tool print before having test case:

![Description of the image](https://github.com/thinhrick0101/demo/blob/main/t%E1%BA%A3i%20xu%E1%BB%91ng%20(8).jpeg)

![Description of the image](https://github.com/thinhrick0101/demo/blob/main/t%E1%BA%A3i%20xu%E1%BB%91ng%20(9).jpeg)

As we see, the branch1 did not hit so I will create a test case for type of textContent = undefined:

![Description of the image](https://github.com/thinhrick0101/demo/blob/main/448460018_1130320471384099_2100954714234095212_n%20(1).png)

And the final result:

![Description of the image](https://github.com/thinhrick0101/demo/blob/main/448368679_2201176123572680_2867262525276031485_n.png)

Function 2: handleKeyDown() function in src/js/close-button.js

The original function:

![Description of the image](https://github.com/thinhrick0101/demo/blob/main/448973953_380649091231315_6296111906017772069_n.png)

The instrument function:

![Description of the image](https://github.com/thinhrick0101/demo/blob/main/448810704_699166539002465_3954360496719867065_n.png)

My coverage print before having test case:

![Description of the image](https://github.com/thinhrick0101/demo/blob/main/448143940_976195600965576_250459141868192700_n.png)

The existing coverage tool for handleKeyDown() function:

![Description of the image](https://github.com/thinhrick0101/demo/blob/main/448136007_891654652797813_8153759499089083295_n.png)

As we see, the branch2 did not hit so I will create the test case for branch 2:

![Description of the image](https://github.com/thinhrick0101/demo/blob/main/448146235_1542578716297224_6913728353682836637_n.png)

And the final result:

![Description of the image](https://github.com/thinhrick0101/demo/blob/main/448124933_1036206201179945_4086439768278396142_n.png)
