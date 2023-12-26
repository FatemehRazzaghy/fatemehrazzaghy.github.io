---
layout: posts
title: Django Project
---
_This is my exercise app_ 

Introduction:<br>
In this blog post, I'll continue exploring the Django project designed for managing body exercises. The focus <br>will be on the role of prompts (parameters) within various functions to handle and display information <br>related to different body sections and exercises.<br>

Functions and Prompts:<br>

1.Function exercise_list:<br>

Prompts: This function, by default, retrieves and displays all exercises and body parts.<br>
Parameters: request (database input)<br>
2.Functions body_part_detail, arm_detail, leg_detail, back_detail, abs_detail:<br>

Prompts: These functions provide information related to various body sections.<br>
Parameters: request (database input) and part (body section)<br>
3.Functions add_exercise and show_exercise:<br>

Prompts: These functions receive and display information about adding new exercises and showing existing ones.<br>
Parameters: request (database input)<br>
4.Functions arm_view, leg_view, abs_view, back_view:<br>

Prompts: These functions display information related to different body sections.<br>
Parameters: request (database input)<br>
Explanations:<br>

In the program, the part parameter serves as a crucial prompt for determining the desired body section. It<br> plays a significant role in fetching section-specific information.<br>
Different functions use prompts to retrieve and display information about exercises and various body sections.<br>
The get_exercises_for_part function is a simple example of how exercises are retrieved based on a specific <br>body section.<br>
The section for adding exercises (add_exercise) uses prompts from the form data in POST requests.<br>
Conclusion:<br>
In this Django project, prompts play a vital role in determining the desired body section and fetching <br>information related to exercises. Each function uses prompts to display information about a specific body <br>section, contributing to the improvement of the program's structure and capabilities.<br>

Project Overview:<br>
This Django project focuses on managing body exercises. It utilizes prompts to enhance the functionality of <br>displaying and handling information about various body sections and exercises.<br>

Stay tuned for more updates on this exciting Django project!<br>

this is my web application link<br>


<a href="http://fatemehrazzaghy.pythonanywhere.com">exercise application</a>






