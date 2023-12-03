# <span id="tjidtitle">Collaborative Document Module</span>

<div>Technologies: <span id="tjidtechs">Yii2, MySQL</span></div>
<br />

I created this module to help a team working on accreditation collaborate effectively while working separately. They were responsible for creating content for a comprehensive accreditation book and collecting necessary reference materials. So, there was a need for a system not just to gather materials but also to manage who can access which documents, keep track of progress, and provide assessment features.

Let's begin by looking at the structure of the data.

I designed 5 tables specifically for this module :
<p align="center">
<img width="60%" alt="buku" src="https://github.com/tambunjb/collaborative-document-module/assets/22196181/f920caff-65d9-42b0-817d-b35e75871cf1">
</p>
1. buku: Book, acts as the main structure where all the book's content is stored.<br />
2. komponen: Component, function as a chapter, section, paragraph, or any breakdown within a book, depending on the user's preference.<br />
3. penulis: Writer, establishes a many-to-many relationship between components and employees, indicating who can access each component.<br />
4. lampiran: Reference, documents used to create content or as attachments.<br />
5. penilai: Assessor, users from the same organization assigned to conduct mock assessments.<br />
<br />
Next, I'll explain how the tool functions with screenshots of the app.
<br /><br />
Firstly, there's a page for managing books, allowing users to create, update, delete, or view books. It also displays the progress of content and reference documents, along with assessments from mock assessors.
<p align="center">
<img width="60%" alt="buku" src="https://github.com/tambunjb/collaborative-document-module/assets/22196181/df8e0c3d-6b27-4a96-b96f-e2aedbd48685">
</p>
<br />
Then, there's a section displaying the content of the book, organized in a tree-like structure of components. This area also tracks progress in content creation, reference documents, and mock assessment grades.
<p align="center">
<img width="60%" alt="komponen" src="https://github.com/tambunjb/collaborative-document-module/assets/22196181/4dbc14c7-41a7-408a-b071-fd9611d30c28">
</p>
<br />
When a user wants to create a new component or sub-component based on the position of a green button in the structure, a form pops up. This form enables users to add a list of writers and assessors.
<p align="center">
<img width="60%" alt="create_komponen" src="https://github.com/tambunjb/collaborative-document-module/assets/22196181/e1aa3433-097f-4ae3-a17f-06c3b9ebcca2">
</p>
<br />
Lastly, there's the view of a component. It shows static details (component name, associated book, description, etc.), forms for updating content and its progress, a review form, mock assessment grades, a list of reference documents, and a form to add more references. It's worth noting that these forms are role-specific, meaning, for instance, the review form appears only for those with the assessor role.
<p align="center">
<img width="60%" alt="komponen_view" src="https://github.com/tambunjb/collaborative-document-module/assets/22196181/f394c353-38e4-400c-a1f7-c26544529fef">
</p>
<br />
That covers the main features of this module. It has proven to be immensely helpful for the organization I worked with, especially for accreditation purposes. It allows teams to collaborate effectively, maintain versioning and track progress securely on their private storage server since this is a private system, rather than relying on third-party services.

