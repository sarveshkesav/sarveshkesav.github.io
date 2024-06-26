<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Research Profile</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        .header {
            background-color: #4CAF50;
            overflow: hidden;
        }
        .header a {
            float: left;
            display: block;
            color: white;
            text-align: center;
            padding: 14px 16px;
            text-decoration: none;
        }
        .header a:hover {
            background-color: #ddd;
            color: black;
        }
        .tabcontent {
            display: none;
            padding: 20px;
        }
        .tabcontent.active {
            display: block;
        }
        .subtabcontent {
            display: none;
            padding: 20px;
            border-top: 1px solid #ddd;
        }
        .subtabcontent.active {
            display: block;
        }
        .subheader {
            background-color: #f1f1f1;
            overflow: hidden;
        }
        .subheader a {
            float: left;
            display: block;
            color: black;
            text-align: center;
            padding: 10px 16px;
            text-decoration: none;
        }
        .subheader a:hover {
            background-color: #ddd;
            color: black;
        }
        .profile-image {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin-right: 20px;
            float: left;
        }
    </style>
</head>
<body>

    <div class="header">
        <a href="#" class="tablink" onclick="openTab(event, 'Profile')" id="defaultOpen">Profile</a>
        <a href="#" class="tablink" onclick="openTab(event, 'ResearchProjects')">My Research Projects</a>
        <a href="#" class="tablink" onclick="openTab(event, 'Publications')">Publications</a>
        <a href="#" class="tablink" onclick="openTab(event, 'TalksAndPosters')">Talks and Posters, Member</a>
    </div>

    <div id="Profile" class="tabcontent">
        <h1>Profile</h1>
        <div class="subheader">
            <a href="#" class="sublink" onclick="openSubTab(event, 'Background')">Background</a>
            <a href="#" class="sublink" onclick="openSubTab(event, 'Education')">Education</a>
            <a href="#" class="sublink" onclick="openSubTab(event, 'Interests')">Interests</a>
        </div>
        <div id="Background" class="subtabcontent active">
            <img src="your-image-url.jpg" alt="Profile Image" class="profile-image">
            <h2>Background</h2>
            <p>Information about my background.</p>
        </div>
        <div id="Education" class="subtabcontent">
            <h2>Education</h2>
            <p>Details about my educational background.</p>
        </div>
        <div id="Interests" class="subtabcontent">
            <h2>Interests</h2>
            <p>My research interests and other areas of interest.</p>
        </div>
    </div>

    <div id="ResearchProjects" class="tabcontent">
        <h1>My Research Projects</h1>
        <div class="subheader">
            <a href="#" class="sublink" onclick="openSubTab(event, 'OngoingProjects')">Ongoing Projects</a>
            <a href="#" class="sublink" onclick="openSubTab(event, 'CompletedProjects')">Completed Projects</a>
        </div>
        <div id="OngoingProjects" class="subtabcontent active">
            <h2>Ongoing Projects</h2>
            <p>Information about my ongoing research projects.</p>
        </div>
        <div id="CompletedProjects" class="subtabcontent">
            <h2>Completed Projects</h2>
            <p>Details about my completed research projects.</p>
        </div>
    </div>

    <div id="Publications" class="tabcontent">
        <h1>Publications</h1>
        <div class="subheader">
            <a href="#" class="sublink" onclick="openSubTab(event, 'JournalPapers')">Journal Papers</a>
            <a href="#" class="sublink" onclick="openSubTab(event, 'ConferencePapers')">Conference Papers</a>
        </div>
        <div id="JournalPapers" class="subtabcontent active">
            <h2>Journal Papers</h2>
            <p>List of my journal papers.</p>
        </div>
        <div id="ConferencePapers" class="subtabcontent">
            <h2>Conference Papers</h2>
            <p>List of my conference papers.</p>
        </div>
    </div>

    <div id="TalksAndPosters" class="tabcontent">
        <h1>Talks and Posters, Member</h1>
        <div class="subheader">
            <a href="#" class="sublink" onclick="openSubTab(event, 'Talks')">Talks</a>
            <a href="#" class="sublink" onclick="openSubTab(event, 'Posters')">Posters</a>
            <a href="#" class="sublink" onclick="openSubTab(event, 'Membership')">Membership</a>
        </div>
        <div id="Talks" class="subtabcontent active">
            <h2>Talks</h2>
            <p>Details of talks I have given.</p>
        </div>
        <div id="Posters" class="subtabcontent">
            <h2>Posters</h2>
            <p>Information about posters I have presented.</p>
        </div>
        <div id="Membership" class="subtabcontent">
            <h2>Membership</h2>
            <p>Memberships and affiliations.</p>
        </div>
    </div>

    <script>
        function openTab(evt, tabName) {
            var i, tabcontent, tablinks, subtabcontent;
            tabcontent = document.getElementsByClassName("tabcontent");
            for (i = 0; i < tabcontent.length; i++) {
                tabcontent[i].style.display = "none";
            }
            tablinks = document.getElementsByClassName("tablink");
            for (i = 0; i < tablinks.length; i++) {
                tablinks[i].className = tablinks[i].className.replace(" active", "");
            }
            document.getElementById(tabName).style.display = "block";
            evt.currentTarget.className += " active";

            // Reset subtabs
            subtabcontent = document.getElementsByClassName("subtabcontent");
            for (i = 0; i < subtabcontent.length; i++) {
                subtabcontent[i].style.display = "none";
            }
            subtabcontent = document.querySelector(`#${tabName} .subtabcontent`);
            if (subtabcontent) {
                subtabcontent.style.display = "block";
            }
        }

        function openSubTab(evt, subTabName) {
            var i, subtabcontent, sublinks;
            subtabcontent = document.getElementsByClassName("subtabcontent");
            for (i = 0; i < subtabcontent.length; i++) {
                subtabcontent[i].style.display = "none";
            }
            sublinks = document.getElementsByClassName("sublink");
            for (i = 0; i < sublinks.length; i++) {
                sublinks[i].className = sublinks[i].className.replace(" active", "");
            }
            document.getElementById(subTabName).style.display = "block";
            evt.currentTarget.className += " active";
        }

        document.getElementById("defaultOpen").click();
    </script>

</body>
</html>
