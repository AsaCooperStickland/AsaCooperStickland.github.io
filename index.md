<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Asa Cooper Stickland</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary-color: #2563eb;
            --secondary-color: #1e40af;
            --accent-color: #3b82f6;
            --text-dark: #1f2937;
            --text-medium: #4b5563;
            --text-light: #6b7280;
            --background: #ffffff;
            --surface: #f8fafc;
            --border: #e5e7eb;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            line-height: 1.6;
            color: var(--text-dark);
            background: var(--background);
            font-size: 16px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            padding: 60px 0 40px;
            background: linear-gradient(135deg, var(--surface) 0%, #ffffff 100%);
            border-bottom: 1px solid var(--border);
        }

        h1 {
            font-size: 3.5rem;
            font-weight: 700;
            color: var(--text-dark);
            margin-bottom: 20px;
            letter-spacing: -0.025em;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .intro {
            font-size: 1.25rem;
            color: var(--text-medium);
            font-weight: 400;
            line-height: 1.7;
            max-width: 700px;
        }

        .intro strong {
            color: var(--primary-color);
            font-weight: 600;
        }

        main {
            padding: 60px 0;
        }

        section {
            margin-bottom: 60px;
        }

        h2 {
            font-size: 2rem;
            font-weight: 600;
            color: var(--text-dark);
            margin-bottom: 30px;
            position: relative;
            padding-bottom: 10px;
        }

        h2:after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: linear-gradient(90deg, var(--primary-color), var(--accent-color));
            border-radius: 2px;
        }

        h3 {
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--text-dark);
            margin-bottom: 15px;
        }

        .education-item, .publication-item {
            margin-bottom: 25px;
            padding: 20px;
            background: var(--surface);
            border-radius: 12px;
            border: 1px solid var(--border);
            transition: all 0.3s ease;
        }

        .education-item:hover, .publication-item:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(37, 99, 235, 0.1);
            border-color: var(--accent-color);
        }

        .publication-item {
            background: linear-gradient(135deg, #ffffff 0%, var(--surface) 100%);
        }

        .publication-title {
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--text-dark);
            margin-bottom: 8px;
            line-height: 1.4;
        }

        .publication-authors {
            color: var(--text-medium);
            margin-bottom: 8px;
            font-size: 0.95rem;
        }

        .publication-description {
            color: var(--text-light);
            font-style: italic;
            margin-bottom: 12px;
            font-size: 0.9rem;
        }

        .publication-link {
            display: inline-block;
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 500;
            padding: 6px 12px;
            background: rgba(37, 99, 235, 0.1);
            border-radius: 6px;
            font-size: 0.9rem;
            transition: all 0.2s ease;
        }

        .publication-link:hover {
            background: var(--primary-color);
            color: white;
            transform: translateY(-1px);
        }

        .education-degree {
            font-weight: 600;
            color: var(--text-dark);
            font-size: 1.1rem;
        }

        .education-school {
            color: var(--text-medium);
            margin-left: 8px;
        }

        .education-year {
            color: var(--text-light);
            font-size: 0.9rem;
            margin-top: 4px;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            padding: 15px 20px;
            background: var(--surface);
            border-radius: 10px;
            border: 1px solid var(--border);
            text-decoration: none;
            color: var(--text-dark);
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(37, 99, 235, 0.15);
            border-color: var(--accent-color);
            color: var(--primary-color);
        }

        .scholar-link {
            display: inline-block;
            color: var(--primary-color);
            text-decoration: none;
            font-weight: 500;
            padding: 12px 24px;
            background: linear-gradient(135deg, rgba(37, 99, 235, 0.1), rgba(59, 130, 246, 0.1));
            border-radius: 8px;
            margin-top: 20px;
            transition: all 0.3s ease;
            border: 1px solid rgba(37, 99, 235, 0.2);
        }

        .scholar-link:hover {
            background: var(--primary-color);
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(37, 99, 235, 0.3);
        }

        footer {
            text-align: center;
            padding: 40px 0;
            color: var(--text-light);
            border-top: 1px solid var(--border);
            background: var(--surface);
            font-size: 0.9rem;
        }

        /* Responsive design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }

            .intro {
                font-size: 1.1rem;
            }

            h2 {
                font-size: 1.75rem;
            }

            .container {
                padding: 0 15px;
            }

            header {
                padding: 40px 0 30px;
            }

            main {
                padding: 40px 0;
            }

            section {
                margin-bottom: 40px;
            }
        }

        /* Smooth animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .education-item, .publication-item {
            animation: fadeInUp 0.6s ease forwards;
        }

        .publication-item:nth-child(2) { animation-delay: 0.1s; }
        .publication-item:nth-child(3) { animation-delay: 0.2s; }
        .publication-item:nth-child(4) { animation-delay: 0.3s; }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Asa Cooper Stickland</h1>
            <p class="intro">
                Welcome to my homepage! I'm a research scientist at the <strong>UK AI Security Institute</strong>, working on AI control and model organisms of misalignment. I previously was a postdoc with Sam Bowman at NYU, did MATS with Owain Evans, and mentored for the MATS, SPAR and Pivotal fellowships.
            </p>
        </div>
    </header>

    <main>
        <div class="container">
            <section>
                <h2>Education</h2>
                <div class="education-item">
                    <div class="education-degree">Ph.D. in Machine Learning</div>
                    <span class="education-school">University of Edinburgh</span>
                    <div class="education-year">2018-2023</div>
                </div>
                <div class="education-item">
                    <div class="education-degree">M.S. in Computer Science</div>
                    <span class="education-school">University of Edinburgh</span>
                    <div class="education-year">2017-2018</div>
                </div>
                <div class="education-item">
                    <div class="education-degree">MPhys in Physics</div>
                    <span class="education-school">Durham University</span>
                    <div class="education-year">2013-2017</div>
                </div>
            </section>

            <section>
                <h2>Publications</h2>
                <h3>Highlighted Research</h3>
                
                <div class="publication-item">
                    <div class="publication-title">Taken out of context: On measuring situational awareness in LLMs</div>
                    <div class="publication-authors">L Berglund, <strong>AC Stickland</strong>, M Balesni, M Kaufmann, M Tong, T Korbak, et al. (2023)</div>
                    <div class="publication-description">Introduces the concept of "out of context learning", and methods for measuring situational awareness in large language models</div>
                    <a href="https://arxiv.org/abs/2309.00667" class="publication-link">Paper</a>
                </div>

                <div class="publication-item">
                    <div class="publication-title">Future events as backdoor triggers: Investigating temporal vulnerabilities in LLMs</div>
                    <div class="publication-authors">S Price, A Panickssery, S Bowman, <strong>AC Stickland</strong> (2024)</div>
                    <div class="publication-description">Language models can trigger backdoors only on future events</div>
                    <a href="https://arxiv.org/abs/2407.04108" class="publication-link">Paper</a>
                </div>

                <div class="publication-item">
                    <div class="publication-title">RepliBench: Evaluating the Autonomous Replication Capabilities of Language Model Agents</div>
                    <div class="publication-authors">S Black, <strong>AC Stickland</strong>, J Pencharz, O Sourbut, M Schmatz, J Bailey, et al. (2025)</div>
                    <div class="publication-description">Benchmark for evaluating AI systems' ability to autonomously replicate themselves</div>
                    <a href="https://arxiv.org/abs/2504.18565" class="publication-link">Paper</a>
                </div>

                <a href="https://scholar.google.com/citations?user=Ljqy-RMAAAAJ&hl=en" class="scholar-link">
                    See full publication list on Google Scholar →
                </a>
            </section>

            <section>
                <h2>Contact</h2>
                <div class="contact-grid">
                    <a href="mailto:asacoopstick@gmail.com" class="contact-item">
                        <span>📧 Email</span>
                    </a>
                    <a href="https://scholar.google.com/citations?user=Ljqy-RMAAAAJ&hl=en" class="contact-item">
                        <span>🎓 Google Scholar</span>
                    </a>
                    <a href="https://twitter.com/AsaCoopStick" class="contact-item">
                        <span>🐦 Twitter</span>
                    </a>
                    <a href="https://www.linkedin.com/in/asa-cooper-stickland-a2712b122/" class="contact-item">
                        <span>💼 LinkedIn</span>
                    </a>
                </div>
            </section>
        </div>
    </main>

    <footer>
        <div class="container">
            <p><em>Last updated: 21/07/2025</em></p>
        </div>
    </footer>
</body>
</html>