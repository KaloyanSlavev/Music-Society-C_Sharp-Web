﻿# Music-Society-Forum 
<div>
    <p>Design and implement a simple Web-based application, e.g. blog / forum.</p>
    <p><strong>Technology:</strong> C# + ASP.NET MVC + Entity Framework + SQL Server + HTML + CSS.</p>
</div>
<strong >Mandatory functionality:</strong>
<ul>
    <li>User registration, login & logout;</li>
    <li>View some content (e.g. blog articles/ publications);</li>
    <li>Create new content (e.g. post new blog article/ publication);</li>
    <li>Use at least 2 tables (collections) with a relationship, e.g. users & blog posts;</li>
    <li>Use a database or a cloud-based backend;</li>
</ul>   
    
<strong >Optional functionality:</strong>
<ul>
    <li>Paging;</li>
    <li>Searching functionality;</li>
    <li>Comments to publications;</li>
    <li>Sidebar holding lists of publications;</li>
    <li>Tags/ Categories for publications;</li>
    <li>Admin panel;</li>
</ul>
   
<strong >Requirements to Individual Projects:</strong>
<ul>
    <li>At least 4 pages (views) & 2 database tables;</li>
    <li>User registration, login, view content, create content;</li>
</ul>

<h3>Implemented Functionality</h3>
<div>
    <p>
        I have developed a <strong>forum for music reviews and recommendations</strong>.
        Music reviews have title, content, author & date and optionally - recommended status, category & comments.
        Comments have content, author and date and refer to a specific music review.
    </p>
    <strong>Users:</strong>
    <ul>
        <li>
            <strong>Anonymous visitors</strong> (users without registration & not logged-in users) can:
            <ul>
                <li>read all reviews & comments;</li>
                <li>search, filter and sort content in reviews & comments;</li>
                <li>register in the forum, login & logout;</li>
                <li>
                    Registered users should have a mandatory full name, email (username) & password. The email (username) should be unique.
                    The password requirements have been simplified – the password should consist of at least 3 characters.
                </li>
            </ul>
        </li>
        <li>
            In addition to the functionality available to anonymous visitors <strong>logged-in users</strong> can:
            <ul>
                <li>create new music reviews & comments;</li>
                <li>edit their own reviews & comments (but not the recommended status on the reviews & the content author);</li>
                <li>delete their own comments;</li>
                <li>delete their reviews if the review does not have any comments.</li>
            </ul>
        </li>
        <li>
            In addition to the above functionality <strong>admins</strong> (users in role “Administrators”) can:
            <ul>
                <li>edit all properties of a publication (incl. the author);</li>
                <li>recommend reviews by modifying the recommended status of a publication;</li>
                <li>delete all publications.</li>
            </ul>
        </li>
    </ul>

    <strong>Views:</strong>
    <ul>
        <li>The <strong>Home page</strong>  shows the latest 5 music reviews (title, date, author & a short content limited to the first 1500 words of the review content).</li>
        <li>The <strong>sidebar</strong> provides links to the latest 5 reviews in several <strong>categories</strong>: recommended reviews, from our editors (users in role “Editors”), most commented, recently commented & top categories.</li>
        <li>Implemented a <strong>search box</strong> for filtering content (searching in title, content, category & author) and <strong>pagination</strong> (5 music reviews per page).</li>
        <li>The <strong>Details view</strong> shows the full content of the selected publication (title, author, date & content) with a respective hyperlink to <strong>List of all Reviews/ Comments</strong>. A hyperlink to <strong>edit</strong> the publication is visible only to admin users and owners. A hyperlink to <strong>delete</strong> the publication is visible to admin users and if the review does not have any comments – to owners. The sidebar provides <strong>previous / next links</strong>  to similar publications (reviews or comments) sorted by date. The <strong>review sidebar</strong> shows the number of comments on the review & all comments in concise form (comment author, date, short comment text limited to 150 words) with hyperlinks to the full comment text. The <strong>comment sidebar</strong>  shows a summary of the commented music review with a hyperlink to the full content.</li>
        <li>The <strong>All Reviews/ All Comments</strong> view shows a table holding all respective publications (title, content, date, author, comments counts and actions). All users (incl. anonymous users) can see the details link. Owners & admins can see the <strong>edit</strong> link. Owners (with permissions to delete) & admins can see the <strong>delete</strong> link. Admin users can see the recommended status of the reviews. A filtering <strong> search box, pagination & sorting on columns </strong> are implemented.</li>
        <li>The <strong>Create</strong> view allows logged-in users to create a new music review after providing title & content. The current date & user identity are provided by the controller.</li>
        <li>The <strong>Edit</strong> view allows logged-in users (owners & admins) to edit the publication title, content & date. Only admins can modify the publication author & the recommended status of a review. A <strong> date-time picker calendar </strong> facilitates the editing of date/time.</li>
        <li>The <strong>Delete</strong> view provides all the details of the selected publication & a delete button. The view is accessible only by admins & owners with permissions to delete. Admins should be able to see all corresponding comments to the review and be able to delete individual comments or the entire review with all its comments.</li>
        <li><strong>My Texts</strong> panel provides links to publications belonging to the current logged-in user.</li>
        <li>The <strong>Admin</strong> panel provides quick view of the <strong>recommended publications</strong> and links to viewing/ editing/ deleting all reviews, comments & categories.</li>
        <li>The <strong>notifications system</strong> provide feedback on users' actions.</li>
        <li>Implemented <strong>Categories</strong> for music Reviews and provided hyperlinks to top categories on the home page</li>
    </ul>
</div>

