# Virtual-CV-code

// Portfolio Website - React Template with Enhancements

import React, { useState } from "react";

const App = () => {
  const [darkMode, setDarkMode] = useState(false);

  return (
    <div className={`${
        darkMode ? "bg-gray-900 text-white" : "bg-gray-50 text-gray-800"
      } font-sans min-h-screen`}>
      <header className="bg-white dark:bg-gray-800 shadow p-6 text-center">
        <h1 className="text-4xl font-bold">Tshegofatso Maloyi</h1>
        <p className="text-xl mt-2">All-Round IT Student | Passionate About Software, Data & Automation</p>
        <button
          onClick={() => setDarkMode(!darkMode)}
          className="mt-4 px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700"
        >
          Toggle {darkMode ? "Light" : "Dark"} Mode
        </button>
      </header>

      <main className="max-w-4xl mx-auto p-6">
        {/* About Me */}
        <section className="my-10">
          <h2 className="text-2xl font-semibold mb-4">About Me</h2>
          <p>
            I am a motivated Information Technology student who thrives on solving challenges through
            software, data, and automation. With a hands-on approach to learning, I build full-stack
            applications, insightful dashboards, and practical automations. I’m always excited to
            explore modern tools and create solutions that make an impact.
          </p>
        </section>

        {/* Resume */}
        <section className="my-10">
          <h2 className="text-2xl font-semibold mb-4">Resume</h2>
          <a
            href="/Rethabile_Fatso_CV.pdf"
            className="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700"
            download
          >
            Download CV
          </a>
        </section>

        {/* Projects */}
        <section className="my-10">
          <h2 className="text-2xl font-semibold mb-4">Projects</h2>
          <ul className="list-disc ml-6">
            <li>
              <strong>Virtual CV Website</strong> – A personal portfolio built using React and hosted on GitHub Pages.
              [<a href="https://github.com/RethabileFatso/virtual-cv" className="text-blue-400 underline">View Code</a>]
            </li>
            <li>
              <strong>Full-Stack Web App</strong> – Group project for CMPG 323 module.
              [<a href="https://github.com/RethabileFatso/cmpg323-project" className="text-blue-400 underline">View Code</a>]
            </li>
          </ul>
        </section>

        {/* Skills */}
        <section className="my-10">
          <h2 className="text-2xl font-semibold mb-4">Skills</h2>
          <div className="grid grid-cols-2 gap-4">
            <span>HTML / CSS / JavaScript</span>
            <span>Python / SQL</span>
            <span>React / Node.js</span>
            <span>Power BI / Git / GitHub</span>
          </div>
        </section>

        {/* Contact */}
        <section className="my-10">
          <h2 className="text-2xl font-semibold mb-4">Contact</h2>
          <form name="contact" method="POST" data-netlify="true" className="space-y-4">
            <input
              type="hidden"
              name="form-name"
              value="contact"
            />
            <input
              type="text"
              name="name"
              placeholder="Your Name"
              className="w-full px-4 py-2 border rounded"
              required
            />
            <input
              type="email"
              name="email"
              placeholder="Your Email"
              className="w-full px-4 py-2 border rounded"
              required
            />
            <textarea
              name="message"
              placeholder="Your Message"
              rows="4"
              className="w-full px-4 py-2 border rounded"
              required
            ></textarea>
            <button type="submit" className="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700">
              Send Message
            </button>
          </form>
          <p className="mt-6">Email: maloyitshegofatso@gmail.com</p>
          <p>GitHub: <a href="https://github.com/RethabileFatso" className="text-blue-400 underline">github.com/RethabileFatso</a></p>
          <p>LinkedIn: <a href="https://www.linkedin.com/in/tshegofatso-maloyi-1159b8298/" className="text-blue-400 underline">linkedin.com/in/tshegofatso-maloyi-1159b8298</a></p>
        </section>
      </main>

      <footer className="text-center py-6 border-t mt-10 text-sm text-gray-600 dark:text-gray-300">
        &copy; {new Date().getFullYear()} Rethabile Fatso
      </footer>
    </div>
  );
};

export default App;
