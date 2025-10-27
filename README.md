<!DOCTYPE html>
<html lang="ar" dir="rtl"> <!-- للعربي، غير dir إلى ltr لو إنجليزي -->
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Projects</title>
    <style>
        body {
            margin: 0;
            padding: 20px;
            background-color: #000; /* أسود زي الصورة */
            font-family: Arial, sans-serif;
            color: white;
        }

        .projects-section {
            max-width: 1200px;
            margin: 0 auto;
        }

        .projects-title {
            text-align: center;
            font-size: 2.5em;
            color: #4CAF50; /* أخضر زي الـ accent */
            margin-bottom: 40px;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* Grid responsive */
            gap: 20px;
        }

        .project-card {
            position: relative;
            background: #111; /* خلفية الكارت */
            border-radius: 15px; /* rounded corners */
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0,0,0,0.3); /* shadow */
            transition: all 0.3s ease; /* انتقال سلس للـ hove   * /
        }

        .project-card:hover {
            transform: translateY(-10px) scale(1.02); /* تكبير ورفع عند hover */
            box-shadow: 0 8px 20px rgba(76, 175, 80, 0.5); /* shadow أقوى مع أخضر */
        }

        .project-image {
            width: 100%;
            height: 200px;
            object-fit: cover; /* الصورة تملأ المساحة بدون تشويه */
            transition: opacity 0.3s ease;
        }

        .project-overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(76, 175, 80, 0.8); /* overlay أخضر شفاف */
            opacity: 0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            transition: opacity 0.3s ease;
        }

        .project-card:hover .project-overlay {
            opacity: 1; /* يظهر الـ overlay عند hover */
        }

        .project-overlay h3 {
            margin: 0;
            font-size: 1.5em;
            color: white;
        }

        .project-overlay p {
            margin: 10px 0 0;
            text-align: center;
            color: white;
            padding: 0 20px;
        }

        .project-info {
            padding: 15px;
        }

        .project-title {
            font-size: 1.2em;
            color: #4CAF50;
            margin: 0 0 10px;
        }

        .project-desc {
            font-size: 0.9em;
            color: #ccc;
            margin: 0;
        }

        /* زر أو أيقونة إضافية زي اللي في الصورة */
        .project-button {
            margin-top: 10px;
            padding: 8px 16px;
            background: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .project-card:hover .project-button {
            opacity: 1;
        }
    </style>
</head>
<body>
    <section class="projects-section">
        <h1 class="projects-title">My Projects</h1>
        <div class="projects-grid">
            <!-- كارت 1: Healthy Foods Project -->
            <div class="project-card">
                <img src="https://via.placeholder.com/300x200/4CAF50/FFFFFF?text=Healthy+Foods" alt="Healthy Foods" class="project-image">
                <div class="project-overlay">
                    <h3>Healthy Foods Project</h3>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc ultricies...</p>
                    <button class="project-button">View Details</button>
                </div>
                <div class="project-info">
                    <h4 class="project-title">Healthy Foods Project</h4>
                    <p class="project-desc">Lorem ipsum dolor sit amet, consectetur.</p>
                </div>
            </div>

            <!-- كارت 2: Another Project -->
            <div class="project-card">
                <img src="https://via.placeholder.com/300x200/2196F3/FFFFFF?text=Another+Project" alt="Project 2" class="project-image">
                <div class="project-overlay">
                    <h3>Another Project</h3>
                    <p>Project description with more details on hover.</p>
                    <button class="project-button">View Details</button>
                </div>
                <div class="project-info">
                    <h4 class="project-title">Another Project</h4>
                    <p class="project-desc">Short description here.</p>
                </div>
            </div>

            <!-- كارت 3: Project 3 -->
            <div class="project-card">
                <img src="https://via.placeholder.com/300x200/FF9800/FFFFFF?text=Project+3" alt="Project 3" class="project-image">
                <div class="project-overlay">
                    <h3>Project 3</h3>
                    <p>Detailed info appears on hover.</p>
                    <button class="project-button">View Details</button>
                </div>
                <div class="project-info">
                    <h4 class="project-title">Project 3</h4>
                    <p class="project-desc">Another short desc.</p>
                </div>
            </div>

            <!-- كارت 4: Project 4 (جديد) -->
            <div class="project-card">
                <img src="https://via.placeholder.com/300x200/E91E63/FFFFFF?text=Project+4" alt="Project 4" class="project-image">
                <div class="project-overlay">
                    <h3>Project 4</h3>
                    <p>Advanced features and modern design for this project.</p>
                    <button class="project-button">View Details</button>
                </div>
                <div class="project-info">
                    <h4 class="project-title">Project 4</h4>
                    <p class="project-desc">New innovative idea.</p>
                </div>
            </div>

            <!-- كارت 5: Project 5 (جديد) -->
            <div class="project-card">
                <img src="https://via.placeholder.com/300x200/9C27B0/FFFFFF?text=Project+5" alt="Project 5" class="project-image">
                <div class="project-overlay">
                    <h3>Project 5</h3>
                    <p>Collaborative tool with real-time updates.</p>
                    <button class="project-button">View Details</button>
                </div>
                <div class="project-info">
                    <h4 class="project-title">Project 5</h4>
                    <p class="project-desc">Team-based development.</p>
                </div>
            </div>

            <!-- كارت 6: Project 6 (جديد) -->
            <div class="project-card">
                <img src="https://via.placeholder.com/300x200/00BCD4/FFFFFF?text=Project+6" alt="Project 6" class="project-image">
                <div class="project-overlay">
                    <h3>Project 6</h3>
                    <p>Final project with full integration and testing.</p>
                    <button class="project-button">View Details</button>
                </div>
                <div class="project-info">
                    <h4 class="project-title">Project 6</h4>
                    <p class="project-desc">Complete portfolio piece.</p>
                </div>
            </div>
        </div>
    </section>
</body>
</html>