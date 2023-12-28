# Introduction to LATEX

Sample article demonstrating basic LaTeX syntax.
<!--more-->



# 1. What is LATEX?
![](https://i.stack.imgur.com/t5VF4.png)

LaTeX is a document markup language that allows users to create high-quality documents with consistent and structured text. It is commonly used by students, educators, and researchers in scientific and technical fields, as well as various other domains.

LaTeX has its precursor in TeX, a formatting language created by Donald Knuth, which was quite challenging to use. Subsequently, Leslie Lamport developed LaTeX based on TeX, introducing numerous improvements and making it popular to this day.

The hallmark of LaTeX is its focus on encouraging users to concentrate on content creation while leaving the formatting to the computer[1].


# 2. Exploring LaTeX
## 2.1. Benefits of LaTeX
- LaTeX offers consistency: line spacing, font size, colors, formatting, and more, allowing you flexibility when switching to different documents.
- It automates many tasks: chapter numbering, header creation, table and image generation, references, and more.
- Automatic and consistent citation of reference documents with a neat presentation format.
- LaTeX enables easy rendering of mathematical equations, for example:
$$E = \frac{mc^2}{\sqrt{1-\frac{v^2}{c^2}}}$$
- LaTeX is efficient for working on large projects, allowing you to format hundreds or thousands of pages within a single low-sized .tex file for easy document management.
- LaTeX now has a vast library of packages that aid users in various tasks such as adding footnotes, creating diagrams, generating tables, and more.
- LaTeX also has specialized packages for scientific paper writing, presentations, and spreadsheet functionality. 

![](https://i.stack.imgur.com/ecqMl.jpg)

***Image 01:*** *One of the benefits LaTeX provides is ease of text formatting.*

## 2.2. Disadvantages of LaTeX.
- It takes time to build a consistent structure for documents, such as formatting for scientific papers.
- Writing in LaTeX can be somewhat akin to programming, making it time-consuming when dealing with minor errors.
- Learning and becoming proficient in LaTeX requires a significant time investment.

## 2.3. Some LaTeX Editors to Consider.
- MiKTeX (Bundle) (Windows)
- **Overleaf (Collaborative Online Editor)**
- Mactex (Bundle) (Mac)
- Texlive (Bundle) (Linux)
- Lyx (Bundle & Editor) (Windows, Mac, Linux)
- Texmaker (Windows, Mac, Linux)

In this article, we will delve into the detailed usage of LaTeX through the Overleaf editor. To get started, you can access Overleaf right [here](https://www.overleaf.com/). 

![](https://www.filepicker.io/api/file/ykJ4U4oRxXjmiuTyJ0QL)
***Image 02:*** *The LaTeX Editing Environment on Overleaf.* 

# 3. Learn about Overleaf.
## 3.1. Key Features of Overleaf.
![](https://images.ctfassets.net/nrgyaltdicpt/5doLOtX69is0i6WIiY4um/6cc9be15c75155e7b93cd4823b742e44/overleaf_wide_colour_green_bg.png)

Overleaf is a free, web-based collaborative LaTeX editor. Overleaf has several distinctive and truly useful features for anyone needing to write and collaborate with various stakeholders.

In this blog, **If you are not already familiar with LaTeX** please refer to some basic LaTeX syntax at [here](https://www.overleaf.com/learn/latex/Free_online_introduction_to_LaTeX_(part_1)). After that, I will provide you with a basic standard for text composition with LaTeX. Don't hesitate to copy the LaTeX code snippets and make gradual adjustments to familiarize yourself!

## 3.2. Creating a LaTeX Project on Overleaf.

**Above all, I still encourage you to learn how to use LaTeX**. LaTeX is not at all difficult to learn, and there is virtually endless information and guidance available on the internet about using LaTeX. You don't need to be an expert in LaTeX (although some commands and usage will be necessary), and you will have an excellent system to automate the organization of your writing.
Let's explore the following steps together.

## Step 1 - Register an Account on Overleaf
To use Overleaf, you'll need to create an account. You can access and register [here](https://www.overleaf.com/register?source=post_page-----6599268c095f----------------------).

## Bước 2 - Create a New Project After Registering on Overleaf

![](https://www.filepicker.io/api/file/tJTSxbxOTdywD4SYmbrW)

1. When you log in, you will see a box labeled **New Project**. Click on this box to start creating a project. A project in Overleaf is a folder containing various files.
2. If you've received a URL in your email from someone with a document, and you're asked to click on the URL to access the document, you already have a document to work on. So, just logging in will take you to that document.
3. When you click on **New Project**, you will see a number of standard templates that Overleaf has prepared for you, such as the **Sample Project**. However, we should begin with a **Blank Project** to get a better understanding of LaTeX operations on Overleaf.

![](https://i.imgur.com/8Nccg2x.png?1)
***Ảnh 03***: *Basic Text Editing Environment on Overleaf.* 

Let's go through it from left to right:
1. At the top, you'll see the **Menu** - this contains functions like Download project, copy project, word count, headings, Git/Dropbox integration, and advanced settings.
![](https://i.imgur.com/81fvwmk.png?1)
2. Also on the left, you'll find a sidebar that resembles a file manager. By default, you select and compile the **main.tex** file. You can upload additional text documents or images. Next to it, occupying about half of the screen is the LaTeX document display with two options: **Source** or **Rich Text**. 
3. The right half of the screen displays the output when you export to PDF format. The document will be compiled and displayed automatically. You can choose **Recompile** to manually update if needed. Under **Recompile**, you can also choose between turning on/off automatic compilation, fast compile (draft mode with quick saving), normal compile, or syntax check before compilation.
![](https://i.imgur.com/igRmUCh.png?1)
4. The next button to focus on is the **Download PDF** button - the second white icon from  **Recompile**. This button quickly saves the document as a PDF.
5. At the top-right corner, you'll find the **Share** button - you can select **Turn on link sharing** to allow anyone with the link to access and edit the document. If it's a private document, you can invite collaborators manually via email.
6. Next to the **Share** button, you'll find the **Submit** button - this allows you to submit your document directly to reputable scientific conferences and journals. It's one of the unique features of **Overleaf**.
7. With the **History**  button next to the **Share** button, you can view the editing history of the document - suitable for backup needs.
![](https://i.imgur.com/gkxJClb.png?1)
8. The last button, **Chat** - this is where you can communicate with collaborators. This keeps you focused on Overleaf instead of having to choose a third-party tool for group communication.

### 3.2.1. About the File Manager Panel in Overleaf.
**Overleaf** provides you with a file manager to store the files you will use in your writing process. These files can be text documents or images (remember to upload PDF documents, images, or text). You can also create new folders where you can store your files.

**Note**: If your project contains many images, you can create separate folders to keep your images organized.

In this guide, we will work with the **main.tex** file that has been pre-created.

### 3.2.2. Understanding the Centre Panel

Think of this area as the primary editing workspace. The Centre Panel will provide you with all the tools and some constraints for editing.

The menu items here do not include buttons to insert images, tables, or citations. Instead, you must use LaTeX code. To have a clearer picture, let's design a workflow for the **main.tex** file.

### 3.2.3. Some Notes When Writing in LaTeX

In general, academic documents such as research papers, scholarly articles, etc., often have common structures, including:

- **Metadata**: This is where you provide the title, author information, date, and other basic details. In LaTeX, you can think of this as the **Front Matter**. In Overleaf, we place the front matter at the beginning of the **main.tex** file. We'll explore this in more detail when we switch to the **Source** view to see the document.

- **Table and figures**: Most academic documents will contain information in the form of tables and figures. If you have many tables and figures, it's a good practice to place them in separate files with names like **fig.tex** and **frames.tex**. This way, you can reference them from within the document, or you can copy and paste the code for tables and figures from those files into the specific part of the document you're writing.

- **Citiation**: As the saying goes, "Quoting a book is like carrying a testimony." Using references and citing them demonstrates respect for the authors who have written and cleverly used recognized knowledge to support your argument.

## 4. Building the First Document on Overleaf

You can access My Overleaf project, copy this piece of code, and paste it into your Overleaf link: https://www.overleaf.com/read/yhkrqpqdhcbj

**Important Note**: Choose the XeLaTeX compiler if you want to test the code snippets.

![](https://i.imgur.com/HbvTcYq.png?1)

### 4.1. Regarding the introduction section, which includes the title of the article and the necessary LaTeX packages

First, you will choose the appropriate document type. For example, here, you choose the document type suitable for writing a scientific research paper on A4-sized paper.
```
\documentclass[a4paper]{article}
```
List of packages used when editing. In the code block below, there are many **%** signs - When you list them at the beginning of a line, that line becomes a comment. With comments, they will only appear in the editing window and will not be included in the final PDF file.
```
% These packages help us type in Vietnamese on LaTeX.
\usepackage[utf8]{inputenc}
% These packages help us insert images on LaTeX
\usepackage{graphicx}
% This is the path to image folder where I created 
\graphicspath{ {./images/} }
```

Next, we will list the title of the article, author's name, and the current date here. You can proceed to change the values below.
```
\title{A Sample Document}
\author{Turio}
\date{\today}
```
### 4.2. Building the main content
So we have completed the introduction section. We will now move on to the crucial part of LaTeX file creation. First, always remember the following syntax:

```
% This line of code acts as a gateway to start building your document.
\begin{document}

% After listing the introductory information, you'll declare it here. 
\maketitle
% \his command makes it easy to switch to a new page. - It's listed here because a standard report often dedicates a full page to the cover page.
\newpage

% ... You can refer to other lines of code on the provided Overleaf link for additional details.

% This line of code is used to end the document; if it's missing, the document will result in an error.
\end{document}
```
### 4.3. Now, let's build chapters and an automatic table of contents.

To create a table of contents, use the following syntax:
```
\tableofcontents
\newpage
```

To declare chapters, use \section, \subsection, and the special thing about LaTeX is that they will automatically update the table of contents. 

```
\section{Chapter 1}
\subsection{Subchapter of chapter 1}
% Subchapters of Chapter 1 can be declared the same way.
```

With chapters added, the table of contents will be automatically updated like this:
![](https://i.imgur.com/q2yW1dP.png?1)

### 4.4. Adding images on Overleaf

To add images, follow these steps:
- Add the image to your Overleaf project. You can create a folder for better organization, as demonstrated below, where I created a folder called **images** to store all the images.
![](https://i.imgur.com/R3e14Tm.png?1)
- Use the following code to add the image to LaTeX:
```
% This is the simplest approach to adding images to LaTeX.
% For more detailed adjustments, consult LaTeX documentation.
\begin{figure}[ht]
\includegraphics[width=\textwidth]{name_of_the_file}
\end{figure}
```

### 4.5. Insert table on Overleaf

Building a sample table can be done using the code below. http://www.tablesgenerator.com/ to create a table and then copy the LaTeX code from the website into your document.

### 4.6. Creating a bibliography and citations in Overleaf
We will build the bibliography and citation in Overleaf can be accomplished with the following code:
```
\begin{thebibliography}{2}
\bibitem{doc1}
Author name, \emph{Tài liệu 1}. Publication.
\bibitem{doc2}
Author name, \emph{Tài liệu 2}. Publication.
\end{thebibliography}
```

With a bibliography in place, you can use the **\cite{The document name is listed in \bibitem}** command to cite sources in your document.

## 5. Conclusion

Every text editor has its own pros and cons. However, if you are heading into research or planning to write academic papers in the future, LaTeX is a suitable choice. Alongside LaTeX, Overleaf is a powerful companion with its online collaborative editing features, helping you connect and work with other project members.

**Team**

## **References**: 

[1] [LateX online course](https://www.overleaf.com/learn/latex/Free_online_introduction_to_LaTeX_(part_1)) compiled by [ Dr John Lees-Miller](https://www.overleaf.com/ourteam) and present in Bristol University.
<br>
[2] [How to use Overleaf to Write your papers](https://medium.com/thoughts-philosophy-writing/how-to-use-overleaf-to-write-your-papers-part-i-basic-minimalist-setup-6599268c095f) - Arindam Basu.
