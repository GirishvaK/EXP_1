# Ex01 Portfolio
## Date:

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
portfolio.html
```
'use client';

import { AnimatePresence, motion } from 'framer-motion';
import { useMemo, useState } from 'react';

let profileImage = '/profile.jpg';

const navItems = [
  { label: 'Home', href: '#home' },
  { label: 'About', href: '#about' },
  { label: 'Skills', href: '#skills' },
  { label: 'Projects', href: '#projects' },
  { label: 'Education', href: '#education' },
  { label: 'Contact', href: '#contact' },
];

const skills = [
  { title: 'Programming', items: ['Python', 'C', 'SQL', 'HTML', 'CSS'] },
  { title: 'Technologies', items: ['Git', 'GitHub', 'VS Code', 'Jupyter Notebook'] },
  { title: 'Core Subjects', items: ['Data Science', 'Software Engineering', 'Computer Architecture', 'Machine Learning (Learning)', 'Prompt Engineering'] },
  { title: 'Soft Skills', items: ['Teamwork', 'Communication', 'Leadership', 'Time Management', 'Problem Solving'] },
];

const projects = [
  {
    title: 'Python Data Analysis',
    description: 'Analyzed datasets using Python, Pandas, and NumPy to generate meaningful insights.',
  },
  {
    title: 'Student Management System',
    description: 'Developed a Python-based application for managing student records efficiently.',
  },
  {
    title: 'Software Engineering Documentation',
    description: 'Prepared requirement analysis, impact analysis, PSP/TSP models, and project planning documents.',
  },
  {
    title: 'Portfolio Website',
    description: 'Designed and developed a modern responsive portfolio website.',
  },
];

const certificates = [
  'Python Programming',
  'Data Science Basics',
  'Software Engineering',
  'Artificial Intelligence Fundamentals',
];

const stats = [
  { label: 'Projects', value: 12 },
  { label: 'Certificates', value: 8 },
  { label: 'Internships', value: 1 },
];

export default function Home() {
  const [theme, setTheme] = useState<'dark' | 'light'>('dark');

  const heroText = useMemo(() => [
    'Computer Science Engineering Student',
    'Python Developer',
    'Data Science Enthusiast',
    'Future AI Engineer',
  ], []);

  return (
    <main className={`min-h-screen bg-[#0F172A] text-white ${theme === 'light' ? 'bg-white text-slate-900' : ''}`}>
      <div className="fixed inset-0 overflow-hidden pointer-events-none">
        <div className="absolute inset-0 bg-[radial-gradient(circle_at_top,_rgba(79,70,229,0.24),_transparent_20%),radial-gradient(circle_at_bottom_right,_rgba(14,165,233,0.18),_transparent_18%)]" />
      </div>
      <div className="relative z-10 px-5 py-5 mx-auto max-w-7xl">
        <header className="flex items-center justify-between gap-4 py-4">
          <div className="text-xl font-semibold tracking-[0.2em] uppercase text-slate-200">Aadhithya V</div>
          <div className="hidden space-x-6 md:flex">
            {navItems.map((item) => (
              <a key={item.href} href={item.href} className="transition text-slate-300 hover:text-white">
                {item.label}
              </a>
            ))}
          </div>
          <button
            onClick={() => setTheme(theme === 'dark' ? 'light' : 'dark')}
            className="px-4 py-2 text-sm rounded-full bg-white/10 shadow-glow hover:bg-white/20"
          >
            {theme === 'dark' ? 'Light Mode' : 'Dark Mode'}
          </button>
        </header>

        <section id="home" className="grid gap-10 py-10 lg:grid-cols-[1.1fr_0.9fr] lg:items-center">
          <motion.div
            initial={{ opacity: 0, y: 30 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.8, ease: 'easeOut' }}
            className="space-y-6"
          >
            <div className="inline-flex items-center gap-3 px-4 py-2 text-sm rounded-full bg-white/5 ring-1 ring-white/10 backdrop-blur">
              <span className="h-2 w-2 rounded-full bg-sky-400" />
              <span>Computer Science Engineering Student</span>
            </div>
            <div className="space-y-4">
              <h1 className="text-4xl font-semibold tracking-tight sm:text-5xl lg:text-6xl">Hi, I&apos;m Aadhithya V</h1>
              <div className="text-lg text-slate-300 sm:text-xl">
                <span className="mr-2">I&apos;m a</span>
                <span className="font-semibold text-transparent bg-gradient-to-r from-cyan-300 via-indigo-400 to-violet-400 bg-clip-text">
                  {heroText.join(' · ')}
                </span>
              </div>
            </div>
            <p className="max-w-2xl text-slate-300 sm:text-lg">
              Passionate about software development, AI, and problem-solving. I enjoy building data-driven applications and learning cutting-edge technologies to deliver clean, efficient solutions.
            </p>
            <div className="flex flex-col gap-3 sm:flex-row">
              <a
                href="#contact"
                className="inline-flex items-center justify-center px-6 py-3 text-sm font-semibold rounded-full bg-gradient-to-r from-primary to-secondary text-slate-900 shadow-glow transition hover:scale-[1.01]"
              >
                Contact Me
              </a>
              <a
                href="#projects"
                className="inline-flex items-center justify-center px-6 py-3 text-sm font-semibold rounded-full border border-white/10 bg-white/5 text-white transition hover:border-white/20"
              >
                View Projects
              </a>
            </div>
          </motion.div>

          <motion.div
            initial={{ opacity: 0, scale: 0.96 }}
            animate={{ opacity: 1, scale: 1 }}
            transition={{ duration: 0.8, ease: 'easeOut', delay: 0.1 }}
            className="relative overflow-hidden rounded-[2rem] border border-white/10 bg-white/5 p-8 shadow-glow backdrop-blur"
          >
            <div className="absolute inset-0 bg-[radial-gradient(circle_at_top_left,_rgba(79,70,229,0.35),_transparent_35%),radial-gradient(circle_at_bottom_right,_rgba(6,182,212,0.25),_transparent_35%)]" />
            <div className="relative space-y-4">
              <div className="overflow-hidden rounded-[1.75rem] bg-slate-900/90 shadow-inner">
                <img src={profileImage} alt="Aadhithya V"className="h-80 w-full rounded-[1.5rem] object-cover shadow-lg"/>
              </div>
              <div className="grid gap-4 sm:grid-cols-2">
                {stats.map((stat) => (
                  <div key={stat.label} className="rounded-3xl bg-white/5 p-5 ring-1 ring-white/10">
                    <p className="text-3xl font-semibold text-white">{stat.value}+</p>
                    <p className="mt-2 text-sm text-slate-300">{stat.label}</p>
                  </div>
                ))}
              </div>
            </div>
          </motion.div>
        </section>

        <section id="about" className="space-y-8 py-10">
          <motion.div
            initial={{ opacity: 0, y: 20 }}
            whileInView={{ opacity: 1, y: 0 }}
            viewport={{ once: true }}
            transition={{ duration: 0.7 }}
            className="rounded-[2rem] border border-white/10 bg-white/5 p-8 shadow-glow backdrop-blur"
          >
            <div className="flex items-center justify-between gap-4">
              <div>
                <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">About Me</p>
                <h2 className="mt-4 text-3xl font-semibold">Who I am</h2>
              </div>
              <div className="rounded-full bg-slate-900/80 px-4 py-2 text-sm text-slate-200">First-year CSE Student</div>
            </div>
            <div className="mt-6 space-y-4 text-slate-300">
              <p>First-year Computer Science Engineering student with a passion for Python, Artificial Intelligence, Data Science, and Software Engineering.</p>
              <p>Fast learner with strong problem-solving skills, eager to find internships and opportunities to grow as a software engineer.</p>
            </div>
          </motion.div>

          <div className="grid gap-6 lg:grid-cols-2">
            <motion.div
              initial={{ opacity: 0, x: -20 }}
              whileInView={{ opacity: 1, x: 0 }}
              viewport={{ once: true }}
              transition={{ duration: 0.7, delay: 0.1 }}
              className="rounded-[2rem] border border-white/10 bg-white/5 p-8 shadow-glow backdrop-blur"
            >
              <h3 className="text-xl font-semibold">What I love working on</h3>
              <ul className="mt-4 space-y-3 text-slate-300">
                <li>AI-powered applications</li>
                <li>Data analysis with Python</li>
                <li>Polished front-end experiences</li>
                <li>Problem-solving with code</li>
              </ul>
            </motion.div>

            <motion.div
              initial={{ opacity: 0, x: 20 }}
              whileInView={{ opacity: 1, x: 0 }}
              viewport={{ once: true }}
              transition={{ duration: 0.7, delay: 0.2 }}
              className="rounded-[2rem] border border-white/10 bg-white/5 p-8 shadow-glow backdrop-blur"
            >
              <h3 className="text-xl font-semibold">My strengths</h3>
              <ul className="mt-4 space-y-3 text-slate-300">
                <li>Adaptable and curious learner</li>
                <li>Collaborative team player</li>
                <li>Clear communicator</li>
                <li>Driven to build real-world projects</li>
              </ul>
            </motion.div>
          </div>
        </section>

        <section id="skills" className="space-y-8 py-10">
          <div className="flex flex-col gap-4 md:flex-row md:items-end md:justify-between">
            <div>
              <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">Skills</p>
              <h2 className="mt-3 text-3xl font-semibold">Technical & soft skills</h2>
            </div>
            <p className="max-w-xl text-slate-300">Animated cards show your programming skills, tools, core subjects, and soft skills in a modern glassmorphism layout.</p>
          </div>

          <div className="grid gap-6 lg:grid-cols-2">
            {skills.map((skill, index) => (
              <motion.div
                key={skill.title}
                initial={{ opacity: 0, y: 20 }}
                whileInView={{ opacity: 1, y: 0 }}
                viewport={{ once: true }}
                transition={{ duration: 0.7, delay: index * 0.1 }}
                className="rounded-[2rem] border border-white/10 bg-white/5 p-8 shadow-glow backdrop-blur"
              >
                <h3 className="text-xl font-semibold">{skill.title}</h3>
                <div className="mt-5 space-y-4">
                  {skill.items.map((item) => (
                    <div key={item} className="space-y-2">
                      <div className="flex items-center justify-between text-sm text-slate-300">
                        <span>{item}</span>
                        <span>90%</span>
                      </div>
                      <div className="h-2 rounded-full bg-white/10">
                        <div className="h-full rounded-full bg-gradient-to-r from-primary to-secondary" style={{ width: '90%' }} />
                      </div>
                    </div>
                  ))}
                </div>
              </motion.div>
            ))}
          </div>
        </section>

        <section id="projects" className="space-y-8 py-10">
          <div>
            <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">Projects</p>
            <h2 className="mt-3 text-3xl font-semibold">Recent work</h2>
          </div>

          <div className="grid gap-6 lg:grid-cols-2">
            {projects.map((project, index) => (
              <motion.article
                key={project.title}
                initial={{ opacity: 0, y: 20 }}
                whileInView={{ opacity: 1, y: 0 }}
                viewport={{ once: true }}
                transition={{ duration: 0.7, delay: index * 0.1 }}
                className="rounded-[2rem] border border-white/10 bg-white/5 p-8 shadow-glow backdrop-blur"
              >
                <div className="flex items-center justify-between gap-3">
                  <div>
                    <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">Featured</p>
                    <h3 className="mt-3 text-2xl font-semibold">{project.title}</h3>
                  </div>
                  <div className="h-12 w-12 rounded-3xl bg-slate-900/80 flex items-center justify-center text-lg text-cyan-300">+</div>
                </div>
                <p className="mt-6 text-slate-300">{project.description}</p>
              </motion.article>
            ))}
          </div>
        </section>

        <section id="education" className="space-y-8 py-10">
          <div>
            <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">Education</p>
            <h2 className="mt-3 text-3xl font-semibold">Academic journey</h2>
          </div>

          <motion.div
            initial={{ opacity: 0, y: 20 }}
            whileInView={{ opacity: 1, y: 0 }}
            viewport={{ once: true }}
            transition={{ duration: 0.7 }}
            className="rounded-[2rem] border border-white/10 bg-white/5 p-8 shadow-glow backdrop-blur"
          >
            <div className="grid gap-4 sm:grid-cols-[1.1fr_0.9fr]">
              <div>
                <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">Bachelor of Engineering</p>
                <h3 className="mt-3 text-2xl font-semibold">Computer Science Engineering</h3>
                <p className="mt-4 text-slate-300">Saveetha Engineering College</p>
              </div>
              <div className="rounded-3xl bg-slate-900/80 px-5 py-4 text-sm text-slate-200">
                Expected Graduation: 2030
              </div>
            </div>
          </motion.div>
        </section>

        <section id="certificates" className="space-y-8 py-10">
          <div>
            <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">Certificates</p>
            <h2 className="mt-3 text-3xl font-semibold">Professional badges</h2>
          </div>
          <div className="grid gap-6 sm:grid-cols-2 lg:grid-cols-4">
            {certificates.map((certificate) => (
              <motion.div
                key={certificate}
                initial={{ opacity: 0, y: 20 }}
                whileInView={{ opacity: 1, y: 0 }}
                viewport={{ once: true }}
                transition={{ duration: 0.7 }}
                className="rounded-[2rem] border border-white/10 bg-white/5 p-6 text-center shadow-glow backdrop-blur"
              >
                <div className="mx-auto mb-4 flex h-14 w-14 items-center justify-center rounded-3xl bg-slate-900/80 text-2xl text-cyan-300">✓</div>
                <p className="font-semibold">{certificate}</p>
              </motion.div>
            ))}
          </div>
        </section>

        <section id="achievements" className="space-y-8 py-10">
          <div>
            <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">Achievements</p>
            <h2 className="mt-3 text-3xl font-semibold">Highlights</h2>
          </div>
          <div className="grid gap-6 md:grid-cols-2 lg:grid-cols-4">
            {['Strong academic performer', 'Passionate self-learner', 'Active in technical learning', 'Building real-world software projects'].map((achievement) => (
              <motion.div
                key={achievement}
                initial={{ opacity: 0, y: 20 }}
                whileInView={{ opacity: 1, y: 0 }}
                viewport={{ once: true }}
                transition={{ duration: 0.7 }}
                className="rounded-[2rem] border border-white/10 bg-white/5 p-6 text-slate-200 shadow-glow backdrop-blur"
              >
                <p>{achievement}</p>
              </motion.div>
            ))}
          </div>
        </section>

        <section id="contact" className="space-y-8 py-10">
          <div className="grid gap-6 lg:grid-cols-[0.95fr_1.05fr]">
            <motion.div
              initial={{ opacity: 0, x: -20 }}
              whileInView={{ opacity: 1, x: 0 }}
              viewport={{ once: true }}
              transition={{ duration: 0.7 }}
              className="rounded-[2rem] border border-white/10 bg-white/5 p-8 shadow-glow backdrop-blur"
            >
              <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">Contact</p>
              <h2 className="mt-3 text-3xl font-semibold">Let&apos;s build something together</h2>
              <p className="mt-4 max-w-xl text-slate-300">Reach out for internships, collaborations, or just to say hi. I&apos;m happy to connect and work on exciting projects.</p>

              <div className="mt-8 space-y-4 text-slate-300">
                <div className="rounded-3xl bg-slate-900/80 p-4">
                  <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">Email</p>
                  <p>aadhithya@example.com</p>
                </div>
                <div className="rounded-3xl bg-slate-900/80 p-4">
                  <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">LinkedIn</p>
                  <p>/in/aadhithya-v</p>
                </div>
                <div className="rounded-3xl bg-slate-900/80 p-4">
                  <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">GitHub</p>
                  <p>/aadhithya-v</p>
                </div>
                <div className="rounded-3xl bg-slate-900/80 p-4">
                  <p className="text-sm uppercase tracking-[0.3em] text-cyan-300">Phone</p>
                  <p>+91 98765 43210</p>
                </div>
              </div>
            </motion.div>

            <motion.form
              initial={{ opacity: 0, x: 20 }}
              whileInView={{ opacity: 1, x: 0 }}
              viewport={{ once: true }}
              transition={{ duration: 0.7, delay: 0.1 }}
              className="rounded-[2rem] border border-white/10 bg-white/5 p-8 shadow-glow backdrop-blur"
            >
              <div className="grid gap-5">
                <label className="space-y-2 text-slate-300">
                  <span className="text-sm font-medium">Name</span>
                  <input
                    type="text"
                    placeholder="Your name"
                    className="w-full rounded-3xl border border-white/10 bg-slate-900/80 px-4 py-3 text-white outline-none transition focus:border-cyan-400"
                  />
                </label>
                <label className="space-y-2 text-slate-300">
                  <span className="text-sm font-medium">Email</span>
                  <input
                    type="email"
                    placeholder="Your email"
                    className="w-full rounded-3xl border border-white/10 bg-slate-900/80 px-4 py-3 text-white outline-none transition focus:border-cyan-400"
                  />
                </label>
                <label className="space-y-2 text-slate-300">
                  <span className="text-sm font-medium">Message</span>
                  <textarea
                    rows={5}
                    placeholder="Tell me about your project"
                    className="w-full rounded-3xl border border-white/10 bg-slate-900/80 px-4 py-3 text-white outline-none transition focus:border-cyan-400"
                  />
                </label>
                <button
                  type="submit"
                  className="inline-flex items-center justify-center rounded-full bg-gradient-to-r from-primary to-secondary px-6 py-3 text-sm font-semibold text-slate-900 transition hover:scale-[1.01]"
                >
                  Send Message
                </button>
              </div>
            </motion.form>
          </div>
        </section>

        <footer className="border-t border-white/10 py-8 text-center text-slate-400">
          Designed & Developed by Aadhithya V © 2026
        </footer>
      </div>
    </main>
  );
}


```

## OUTPUT

<img width="1756" height="896" alt="image" src="https://github.com/user-attachments/assets/f70aeb29-00fa-4d38-a293-f661db81288a" />

<img width="1787" height="757" alt="633055841-716e65f3-3d89-4ab2-b91a-380c9af26237" src="https://github.com/user-attachments/assets/10e9f3b4-fa93-4d6c-929b-3caab85f081e" />

<img width="1757" height="672" alt="633056105-3b62a84c-3701-4368-9980-ae1d43b56175" src="https://github.com/user-attachments/assets/8ea15fec-7399-43f7-a36f-3c9cd4fc9ecf" />

<img width="1701" height="552" alt="image" src="https://github.com/user-attachments/assets/514750c6-e243-459b-ac42-a5bca2509ad5" />

<img width="1757" height="816" alt="image" src="https://github.com/user-attachments/assets/09a90220-3d78-438b-b3e6-89ae616fb83f" />

<img width="1761" height="925" alt="image" src="https://github.com/user-attachments/assets/f6f810a0-3953-4ceb-bf73-df922132a0e0" />

<img width="1757" height="827" alt="image" src="https://github.com/user-attachments/assets/95bfffeb-159e-478f-b69c-9fa336b07677" />



## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
