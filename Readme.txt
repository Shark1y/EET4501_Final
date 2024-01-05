
COMPUTER USER BEHAVIOUR DATASET. PC Features

https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7270191/

The monitored keys were:


list_all_keys = 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a, b, c, d, e, f, g, h, i,j, k, l, m, n, ñ, o, p, q, r, s, t, u, v, w, x, y, z, ´,`, ', ", ç, \^, º, @, \$, \%, \&, /, (, ), =, +, |, 'leftwindows', 'crtl', 'shift', 'capslock', 'tab', º, ª, \textbackslash, \#, 'esc', 'f1', 'f2', 'f3', 'f4', 'f5', 'f6', 'f7', 'f8', 'f9', 'f10', 'f11', 'f12', 'PrtSc', 'insert', 'delete', 'home', 'ind', 'pageup', 'pagedown', 'numlock', \}, \{, -, _, '.', ',', [, ], *, <, >, 'space', 'tab', 'inter', 'rightctrl', 'rightshift', 'backspace', 'atlgr', 'alt', 'left', 'right', 'up', 'down', 'rightarrow', 'leftarrow', 'uparrow', 'downarrow'

list_chars = 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, a, b, c, d, e, f, g, h, i, j, k, l, m, n, ñ, o, p, q, r, s, t, u, v, w, x, y, z, ç

list_space = -, _, '.', ',', /, \&, +, <, space, tab, enter, (, ), =, |, \textbackslash, \#


Te generated features are:


    - timestamp. This is the timestamp when the vector generated. It contains a numerical value corresponding to the milliseconds elapsed since the UNIX epoch, 1st January 1970.

    - keystroke_counter. This feature stores the total number of keystrokes produced by the user during the window.

    - erase_keys_counter. This feature stores the number of presses of erasing keys. This is, the keystrokes on 'delete' and 'backspace' keys.

    - erase_keys_percentage. This is the percentage of erasing keystrokes over the total number of keystrokes.

    - press_press_average_interval. This is the average time elapsed between two consecutive keystrokes, measured in milliseconds.

    - press_press_stddev_interval. This is the standard deviation on the time elapsed between two consecutive keystrokes, measured in milliseconds. 

    - press_release_average_interval. This is the average time elapsed between the press and the release of all the keystrokes occurred during the time window, measured in milliseconds.

    - press_release_stddev_interval. This is the standard deviation of the time elapsed between the press and the release of all the keystrokes occurred during the time window, measured in milliseconds.

    - word_counter. This feature represents the total number of words typed by the user during the time window. To determine if the user has written a word, list_chars list is used as word characters and list_space list is used as word delimiter characters.

    - word_average_length. This feature represents the average length of all the words written during the time window.

    - word_stddev_length. This feature represents the standard deviation of the length of all the words written during the time window.

    - word_length_N. This set of features represent the length histogram of the words written during the time window. N ranges from 1 to 11, the words larger than 11 characters are assigned to the 11 box.

    - keystrokes_key_K. This set of features counters the number of keystrokes per key. K is the list of all possible keys. This is, the characters in list_all_keys list previously defined.

    - press_release_average_K. This set of features represent the average time elapsed between the press and the release of each key, measured in milliseconds. Again, there is a feature per character in list_all_keys.

    -  digraph_counter_KK. This set of features counters the number of two keys combinations (digraph) introduced by the user. K is the list of all possible keys (list_all_keys), so there is a combination for each possible key pair. The features of the digraphs that were not entered during the window will have 0 value.

    -  digraph_average_time_KK. This set of features represents the average time elapsed to press each possible digraph, measured in milliseconds. Again, K is each possible character (list_all_keys), so there is a combination for each possible key pair.

    -  click_speed_average_N. This set of features represents the average time elapsed to complete a click using the mouse (button press-release time). N represent each one of the mouse buttons, 0 is left button click, 1 is right button click, 2 is left button double click and 3 is middle button click. These features are measured in milliseconds.

    -  click_speed_stddev_N. This set of features represents the standard deviation of the time elapsed to complete a click using the mouse (button press-release time). N represent each one of the mouse buttons: 0 is left button single click, 1 is right button click, 2 is left button double click and 3 is middle button click. These features are measured in milliseconds.

    -  mouse_action_counter_N. This set of features counters the number of events related to the mouse activity. N represent each possible action: 0, is left button single click, 1 is right button click, 2 is left button double click, 3 is scroll action, 4 is mouse pointer movement, 5 is drag or selection action (left press-movement-release), 6 is middle button click.

    -  mouse_position_histogram_N. This set of features counters the number of mouse events occurred in each quadrant of the screen. Screen is organized in 9 quadrants, dividing the screen size into 3 values in width and 3 in height 3. Then, N goes from 1 to 9.

    -  mouse_movement_direction_histogram_N. This set of features represents the number of mouse movement events in each direction, organized in 8 cardinal points based on the movement angle. N goes from 1 to 8.

    -  mouse_movement_length_histogram_N. This set of features represents the length histogram of the mouse movements occurred during the time window. N has 3 possible values, 1: the movement length is less than a third of the screen size, 2: the movement length is between 1/3 and 2/3 of the screen size, 3: the movement length is larger than 2/3 of the screen size.

    -  mouse_average_movement_duration. This feature represents the average duration of the mouse movements, measured in milliseconds.

    -  mouse_average_movement_speed. This feature represents the standard deviation of the duration of the mouse movements, measured in milliseconds.

    -  mouse_average_movement_speed_direction_N. This set of features represents the histogram of movement average speeds per direction. N goes from 1 to 8 like the movement direction histogram (see \figurename~\ref{fig:mouse_direction}).

    -  active_apps_average. This feature measures the average number of applications active during the time window.

    -  current_app. This feature contains the application in foreground when the vector was generated, it contains a string with the application executable name.

    -  penultimate_app. This feature contains the penultimate application in foreground during the time window, as a string with the application executable name. If only one application was used during the time window, this application will have '-' as value.

    -  changes_between_apps. This feature contains the number of changes between different foreground applications during the time window.

    -  current_app_foreground_time. This feature contains the number of seconds that the current application has been in foreground during the time window. If no application changes occur, this feature will value 60.

    -  current_app_average_processes. This feature represents the average number of processes that the current application in foreground had active during the time window.

    -  current_app_stddev_processes. This feature represents the standard deviation of the number of processes that the current application in foreground had active during the time window.

    -  current_app_average_cpu. This feature represents the average percentage of CPU utilised by the current application during the time window.

    -  current_app_stddev_cpu. This feature represents the standard deviation of the percentage of CPU utilised by the current application during the time window.

    -  system_average_cpu. This feature represents the average of the percentage of system CPU capacity used in total during the time window.

    -  system_stddev_cpu. This feature represents the standard deviation of the percentage of system CPU capacity used in total during the time window.

    -  current_app_average_mem. This feature represents the average memory percentage utilised by the current application during the time window.

    -  current_app_stddev_mem. This feature represents the standard deviation of the percentage of memory utilised by the current application during the time window.

    -  system_average_mem. This feature represents the average of the percentage of system memory capacity used in total during the time window.

    -  system_stddev_mem. This feature represents the standard deviation of the percentage of system memory capacity used in total during the time window.

    - received_bytes. Number of bytes received through the network interfaces of the device during the time window.

    - sent_bytes. Number of bytes sent using the network interfaces of the device during the time window.

    - USER. Label representing to which user the vector belongs. In this dataset, USER label is a number from 0 to 11.

