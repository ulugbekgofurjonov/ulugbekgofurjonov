// Tech Stack component — react-icons ishlatgan holda
// npm install react-icons

import { 
  FaHtml5, FaCss3Alt, FaReact, FaGitAlt, FaGithub, FaFigma 
} from "react-icons/fa";
import { 
  SiJavascript, SiTypescript, SiNextdotjs, SiTailwindcss, 
  SiSass, SiVite, SiVercel, SiRedux
} from "react-icons/si";
import { VscVscode } from "react-icons/vsc";

const techs = [
  { icon: <FaHtml5 />,        name: "HTML5",      color: "#E34F26" },
  { icon: <FaCss3Alt />,      name: "CSS3",       color: "#1572B6" },
  { icon: <SiJavascript />,   name: "JavaScript", color: "#F7DF1E" },
  { icon: <SiTypescript />,   name: "TypeScript", color: "#3178C6" },
  { icon: <FaReact />,        name: "React",      color: "#61DAFB" },
  { icon: <SiNextdotjs />,    name: "Next.js",    color: "#ffffff" },
  { icon: <SiRedux />,        name: "Redux",      color: "#764ABC" },
  { icon: <SiTailwindcss />,  name: "Tailwind",   color: "#38BDF8" },
  { icon: <SiSass />,         name: "Sass",       color: "#CC6699" },
  { icon: <SiVite />,         name: "Vite",       color: "#646CFF" },
  { icon: <FaGitAlt />,       name: "Git",        color: "#F05032" },
  { icon: <FaGithub />,       name: "GitHub",     color: "#ffffff" },
  { icon: <VscVscode />,      name: "VS Code",    color: "#007ACC" },
  { icon: <FaFigma />,        name: "Figma",      color: "#F24E1E" },
  { icon: <SiVercel />,       name: "Vercel",     color: "#ffffff" },
];

export default function TechStack() {
  return (
    <div style={{
      background: "#0D1117",
      minHeight: "100vh",
      display: "flex",
      flexDirection: "column",
      alignItems: "center",
      justifyContent: "center",
      fontFamily: "'Fira Code', monospace",
      padding: "40px 20px"
    }}>
      <h2 style={{ color: "#58A6FF", marginBottom: 8, fontSize: 22 }}>
        🛠️ Tech Stack
      </h2>
      <p style={{ color: "#8B949E", marginBottom: 32, fontSize: 14 }}>
        react-icons orqali chaqirilgan ikonalar
      </p>

      <div style={{
        display: "flex",
        flexWrap: "wrap",
        gap: 16,
        maxWidth: 640,
        justifyContent: "center"
      }}>
        {techs.map(({ icon, name, color }) => (
          <div
            key={name}
            style={{
              display: "flex",
              flexDirection: "column",
              alignItems: "center",
              gap: 6,
              background: "#161B22",
              border: "1px solid #30363D",
              borderRadius: 12,
              padding: "14px 18px",
              cursor: "default",
              transition: "all 0.2s ease",
              minWidth: 72,
            }}
            onMouseEnter={e => {
              e.currentTarget.style.borderColor = color;
              e.currentTarget.style.transform = "translateY(-4px)";
              e.currentTarget.style.boxShadow = `0 8px 24px ${color}33`;
            }}
            onMouseLeave={e => {
              e.currentTarget.style.borderColor = "#30363D";
              e.currentTarget.style.transform = "translateY(0)";
              e.currentTarget.style.boxShadow = "none";
            }}
          >
            <span style={{ fontSize: 32, color, display: "flex" }}>
              {icon}
            </span>
            <span style={{ color: "#8B949E", fontSize: 11, letterSpacing: 0.5 }}>
              {name}
            </span>
          </div>
        ))}
      </div>

      <div style={{
        marginTop: 48,
        background: "#161B22",
        border: "1px solid #30363D",
        borderRadius: 12,
        padding: "20px 28px",
        maxWidth: 500,
        width: "100%"
      }}>
        <p style={{ color: "#58A6FF", fontSize: 13, marginBottom: 12 }}>
          📦 O'rnatish:
        </p>
        <code style={{ color: "#7EE787", fontSize: 13, display: "block" }}>
          npm install react-icons
        </code>
        <p style={{ color: "#8B949E", fontSize: 12, marginTop: 12 }}>
          📌 Import qilish:
        </p>
        <code style={{ color: "#FFA657", fontSize: 12, display: "block", lineHeight: 1.8 }}>
          {`import { FaReact } from "react-icons/fa"`}<br/>
          {`import { SiTailwindcss } from "react-icons/si"`}<br/>
          {`import { VscVscode } from "react-icons/vsc"`}
        </code>
      </div>
    </div>
  );
}
