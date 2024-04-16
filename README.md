# software_copyright_src_format
CN Software copyright source code format tools

## Usage

1. Prepare the source code file to be formatted, and put it in the `source_code` directory.
2. Run the `copyright_format.py` script in the root directory of the project with the custom parameters.

Parameters statement:
| Parameter    | Description                                                                  | Required | Default       |
| ------------ | ---------------------------------------------------------------------------- | -------- | ------------- |
| --template   | The path of the template file                                                | False    | template.docx |
| --src        | The path of the source code directory                                        | False    | source_code   |
| --output     | The path of the output file, it's named will be used to format document head | False    | example.docx  |
| --version    | The version of the software                                                  | False    | 1.0           |
| --black_list | The file suffixes that need to be ignored, separated by spaces               | False    | "png jpg"     |


## Example

source_code structure:

```shell
└─source_code
    ├─安卓客户端
    │  │  http.js
    │  │  
    │  ├─components
    │  │      imagePicker.js
    │  │      SearchablePicker.js
    │  │      
    │  ├─screen
    │  │      calendar.js
    │  │      community.js
    │  │      CommunityDetail.js
    │  │      courseCard.js
    │  │      courseFinish.js
    │  │      courses.js
    │  │      course_details.js
    │  │      FollowersScreen.js
    │  │      FollowingScreen.js
    │  │      LoginScreen.js
    │  │      person.js
    │  │      person_details.js
    │  │      publish.js
    │  │      register.js
    │  │      search.js
    │  │      video.js
    │  │      weekCalendar.js
    │  │
    │  └─services
    │          courses.service.js
    │          fits.service.js
    │          moments.service.js
    │          upload.service.js
    │          users.service.js
    │
    └─服务器端
        │  app.js
        │
        ├─config
        │      db.config.js
        │
        ├─controllers
        │      courses.controller.js
        │      file.controller.js
        │      fits.controller.js
        │      moments.controller.js
        │      users.controller.js
        │
        ├─middleware
        │      imageCompressor.js
        │      upload.js
        │
        ├─models
        │      courses.model.js
        │      fits.model.js
        │      index.js
        │      moments.model.js
        │      poses.model.js
        │      users.model.js
        │
        ├─routes
        │      courses.routes.js
        │      fits.routes.js
        │      index.js
        │      moments.routes.js
        │      users.routes.js
        │
        └─views
                error.jade
                index.jade
                layout.jade
```

Then run the following command:

```shell
 python copyright_format.py --template template.docx --src source_code --output example.docx --version 1.0 --black_list "png jpg"
```
