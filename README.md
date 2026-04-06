

import { motion } from "framer-motion";
import {
  Github,
  Mail,
  Shield,
  Brain,
  Trophy,
  Code2,
  ExternalLink,
  MapPin,
  GraduationCap,
  UserRound,
  TerminalSquare,
  Gamepad2,
  ChevronRight,
} from "lucide-react";
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
import { Badge } from "@/components/ui/badge";
import { Button } from "@/components/ui/button";

const skills = {
  languages: ["C++", "Python", "Java", "JavaScript"],
  web: ["HTML", "CSS"],
  tools: ["Git", "Linux", "VS Code"],
};

const focusAreas = [
  {
    title: "AI Engineering",
    icon: Brain,
    description:
      "Building practical intuition in machine learning through competitions, model experiments, and problem-driven learning.",
  },
  {
    title: "Cybersecurity / CTF",
    icon: Shield,
    description:
      "Developing hands-on skills in web security, cryptography, and structured technical problem solving through CTF challenges.",
  },
  {
    title: "Competitive Programming",
    icon: Trophy,
    description:
      "Strengthening algorithmic thinking, speed, and precision with Python and C++ through continuous practice.",
  },
];

const experience = [
  {
    title: "Captain — NOTFOUND_404 Team",
    icon: Shield,
    description:
      "Leading a team focused on CTF challenges, technical coordination, strategy, and decision-making.",
  },
  {
    title: "CTF Participant",
    icon: TerminalSquare,
    description:
      "Experience in Web, Cryptography, and general challenge-based problem solving.",
  },
  {
    title: "AI Engineering (Junior Level)",
    icon: Brain,
    description:
      "Practical exposure to AI concepts through competitions and self-learning, with a steady focus on models, data thinking, and applied problem solving.",
  },
  {
    title: "Algorithmic Problem Solving",
    icon: Code2,
    description:
      "Strong logic foundation built through consistent practice in Python and algorithmic challenges.",
  },
  {
    title: "Front-End Development",
    icon: Code2,
    description:
      "Built simple, responsive web interfaces using HTML, CSS, and JavaScript.",
  },
  {
    title: "Game Development",
    icon: Gamepad2,
    description:
      "Worked on small-scale game projects focused on gameplay logic and core mechanics.",
  },
];

const projects = [
  {
    title: "CNN Image Classification",
    description:
      "Developed an image classification model using Convolutional Neural Networks, with hands-on work in preprocessing, training, and evaluation.",
    tags: ["Python", "CNN", "Computer Vision", "Deep Learning"],
    link: "https://github.com/BeBecpp/CNN-Image-Classification",
    featured: true,
  },
  {
    title: "Front-End Web Project",
    description:
      "Created a responsive interface using HTML, CSS, and JavaScript with focus on layout, structure, and user interaction.",
    tags: ["HTML", "CSS", "JavaScript"],
    link: "https://github.com/bebecpp",
  },
  {
    title: "Game Development Project",
    description:
      "Built a small-scale game with custom gameplay logic and basic mechanics implementation.",
    tags: ["Game Logic", "Programming", "Project Based Learning"],
    link: "https://github.com/bebecpp",
  },
  {
    title: "Algorithm Practice",
    description:
      "Solved a wide range of algorithmic problems to improve speed, efficiency, and structured problem solving.",
    tags: ["Python", "C++", "Algorithms", "Problem Solving"],
    link: "https://github.com/bebecpp",
  },
];

const fadeUp = {
  hidden: { opacity: 0, y: 22 },
  visible: { opacity: 1, y: 0 },
};

function SectionTitle({ eyebrow, title, description }: { eyebrow: string; title: string; description?: string }) {
  return (
    <div className="mb-8">
      <p className="mb-3 text-xs font-semibold uppercase tracking-[0.35em] text-cyan-400/80">{eyebrow}</p>
      <h2 className="text-2xl font-bold tracking-tight text-white md:text-4xl">{title}</h2>
      {description ? <p className="mt-3 max-w-3xl text-sm leading-7 text-slate-300 md:text-base">{description}</p> : null}
    </div>
  );
}

function SkillGroup({ title, items }: { title: string; items: string[] }) {
  return (
    <Card className="border-white/10 bg-white/5 backdrop-blur-sm">
      <CardHeader>
        <CardTitle className="text-white">{title}</CardTitle>
      </CardHeader>
      <CardContent className="flex flex-wrap gap-2">
        {items.map((item) => (
          <Badge key={item} variant="secondary" className="border border-cyan-400/20 bg-cyan-400/10 px-3 py-1 text-cyan-100 hover:bg-cyan-400/20">
            {item}
          </Badge>
        ))}
      </CardContent>
    </Card>
  );
}

export default function BebePortfolio() {
  return (
    <div className="min-h-screen bg-slate-950 text-slate-100">
      <div className="fixed inset-0 -z-10 overflow-hidden">
        <div className="absolute left-[-8rem] top-[-4rem] h-72 w-72 rounded-full bg-cyan-500/20 blur-3xl" />
        <div className="absolute right-[-6rem] top-40 h-72 w-72 rounded-full bg-fuchsia-500/15 blur-3xl" />
        <div className="absolute bottom-[-4rem] left-1/3 h-72 w-72 rounded-full bg-emerald-500/10 blur-3xl" />
        <div className="absolute inset-0 bg-[linear-gradient(rgba(255,255,255,0.03)_1px,transparent_1px),linear-gradient(90deg,rgba(255,255,255,0.03)_1px,transparent_1px)] bg-[size:36px_36px]" />
        <div className="absolute inset-0 bg-[radial-gradient(circle_at_top,rgba(15,23,42,0)_0%,rgba(2,6,23,0.85)_50%,rgba(2,6,23,1)_100%)]" />
      </div>

      <main className="mx-auto max-w-7xl px-6 py-8 md:px-8 lg:px-10">
        <motion.section
          initial="hidden"
          animate="visible"
          variants={fadeUp}
          transition={{ duration: 0.6 }}
          className="relative overflow-hidden rounded-[32px] border border-white/10 bg-white/5 p-6 shadow-2xl backdrop-blur-md md:p-10"
        >
          <div className="absolute inset-0 bg-gradient-to-br from-cyan-400/10 via-transparent to-fuchsia-500/10" />
          <div className="relative grid gap-10 lg:grid-cols-[1.3fr_0.9fr] lg:items-center">
            <div>
              <div className="mb-4 inline-flex items-center gap-2 rounded-full border border-cyan-400/20 bg-cyan-400/10 px-3 py-1 text-xs font-medium text-cyan-200">
                <span className="h-2 w-2 rounded-full bg-cyan-400" />
                Building toward elite-level technical work
              </div>

              <h1 className="max-w-4xl text-4xl font-black tracking-tight text-white md:text-6xl">
                Bayarbayasgalan Enkhtulga <span className="text-cyan-400">(BeBe)</span>
              </h1>

              <p className="mt-4 text-lg font-medium text-slate-200 md:text-2xl">
                nero_404 · AI Engineering · Cybersecurity · Competitive Programming
              </p>

              <div className="mt-5 flex flex-wrap items-center gap-4 text-sm text-slate-300">
                <div className="flex items-center gap-2">
                  <MapPin className="h-4 w-4 text-cyan-400" />
                  Darkhan, Mongolia
                </div>
                <div className="flex items-center gap-2">
                  <GraduationCap className="h-4 w-4 text-cyan-400" />
                  Secondary School No.31
                </div>
                <div className="flex items-center gap-2">
                  <UserRound className="h-4 w-4 text-cyan-400" />
                  High School Student
                </div>
              </div>

              <p className="mt-6 max-w-3xl text-sm leading-8 text-slate-300 md:text-base">
                I am a high school student from Mongolia focused on building strong, real-world skills in Artificial Intelligence,
                Cybersecurity, and algorithmic problem solving. What began as curiosity has become a clear direction: consistent
                practice, technical competitions, and project-based learning that steadily move me toward high-impact engineering.
              </p>

              <div className="mt-8 flex flex-wrap gap-3">
                <Button asChild size="lg" className="rounded-2xl bg-cyan-500 text-slate-950 hover:bg-cyan-400">
                  <a href="https://github.com/bebecpp" target="_blank" rel="noreferrer">
                    <Github className="mr-2 h-4 w-4" />
                    View GitHub
                  </a>
                </Button>
                <Button asChild size="lg" variant="outline" className="rounded-2xl border-white/15 bg-white/5 text-white hover:bg-white/10">
                  <a href="mailto:bayarbayasgalan.bb@gmail.com">
                    <Mail className="mr-2 h-4 w-4" />
                    Contact Me
                  </a>
                </Button>
              </div>
            </div>

            <div className="grid gap-4 md:grid-cols-2 lg:grid-cols-1 xl:grid-cols-2">
              <Card className="rounded-[24px] border-cyan-400/20 bg-slate-900/70 backdrop-blur-sm">
                <CardContent className="p-6">
                  <div className="text-sm text-slate-400">Primary Focus</div>
                  <div className="mt-2 text-2xl font-bold text-white">AI + Security</div>
                  <p className="mt-3 text-sm leading-7 text-slate-300">
                    Growing through competitions, technical exploration, and practical project work.
                  </p>
                </CardContent>
              </Card>

              <Card className="rounded-[24px] border-fuchsia-400/20 bg-slate-900/70 backdrop-blur-sm">
                <CardContent className="p-6">
                  <div className="text-sm text-slate-400">Competition Status</div>
                  <div className="mt-2 text-2xl font-bold text-white">National AI Stage 2</div>
                  <p className="mt-3 text-sm leading-7 text-slate-300">
                    Advanced to the second stage of a national AI Engineering competition in Mongolia.
                  </p>
                </CardContent>
              </Card>

              <Card className="rounded-[24px] border-emerald-400/20 bg-slate-900/70 backdrop-blur-sm md:col-span-2 lg:col-span-1 xl:col-span-2">
                <CardContent className="p-6">
                  <div className="text-sm text-slate-400">Mindset</div>
                  <div className="mt-2 text-2xl font-bold text-white">Hands-on over passive</div>
                  <p className="mt-3 text-sm leading-7 text-slate-300">
                    I prefer learning by building, solving, competing, and testing ideas in practice instead of only studying theory.
                  </p>
                </CardContent>
              </Card>
            </div>
          </div>
        </motion.section>

        <motion.section
          initial="hidden"
          whileInView="visible"
          viewport={{ once: true, amount: 0.2 }}
          variants={fadeUp}
          transition={{ duration: 0.6, delay: 0.05 }}
          className="mt-24"
        >
          <SectionTitle
            eyebrow="Profile"
            title="A focused path built from curiosity"
            description="My background started with early exposure to technology through my father, who works in IT. That environment made computers feel natural and pushed me toward systems, logic, and technical problem solving from a young age."
          />

          <div className="grid gap-6 lg:grid-cols-2">
            <Card className="rounded-[28px] border-white/10 bg-white/5 backdrop-blur-sm">
              <CardContent className="p-7">
                <h3 className="text-xl font-semibold text-white">Background</h3>
                <p className="mt-4 text-sm leading-8 text-slate-300 md:text-base">
                  I began programming around four years ago with C++ and algorithmic thinking. Since then, I have been growing through
                  continuous self-learning, competitions, and practical technical work. Over time, that early curiosity evolved into a
                  structured direction centered on AI engineering, cybersecurity, and competitive programming.
                </p>
              </CardContent>
            </Card>

            <Card className="rounded-[28px] border-white/10 bg-white/5 backdrop-blur-sm">
              <CardContent className="p-7">
                <h3 className="text-xl font-semibold text-white">Current Direction</h3>
                <p className="mt-4 text-sm leading-8 text-slate-300 md:text-base">
                  I am actively sharpening my skills in AI engineering, CTF-style cybersecurity, and algorithmic problem solving. I am also
                  aiming to join stronger technical environments in the future and contribute to meaningful real-world projects.
                </p>
              </CardContent>
            </Card>
          </div>
        </motion.section>

        <motion.section
          initial="hidden"
          whileInView="visible"
          viewport={{ once: true, amount: 0.2 }}
          variants={fadeUp}
          transition={{ duration: 0.6, delay: 0.08 }}
          className="mt-24"
        >
          <SectionTitle
            eyebrow="Focus Areas"
            title="What I am actively building"
            description="I am currently investing most of my time in three areas that strengthen both technical depth and problem solving discipline."
          />

          <div className="grid gap-6 md:grid-cols-2 xl:grid-cols-3">
            {focusAreas.map((item) => {
              const Icon = item.icon;
              return (
                <Card key={item.title} className="rounded-[28px] border-white/10 bg-white/5 transition-transform duration-300 hover:-translate-y-1 hover:border-cyan-400/30 hover:bg-white/10">
                  <CardContent className="p-7">
                    <div className="flex h-12 w-12 items-center justify-center rounded-2xl bg-cyan-400/10 text-cyan-300">
                      <Icon className="h-6 w-6" />
                    </div>
                    <h3 className="mt-5 text-xl font-semibold text-white">{item.title}</h3>
                    <p className="mt-3 text-sm leading-7 text-slate-300">{item.description}</p>
                  </CardContent>
                </Card>
              );
            })}
          </div>
        </motion.section>

        <motion.section
          initial="hidden"
          whileInView="visible"
          viewport={{ once: true, amount: 0.15 }}
          variants={fadeUp}
          transition={{ duration: 0.6, delay: 0.1 }}
          className="mt-24"
        >
          <SectionTitle
            eyebrow="Experience"
            title="Practical exposure across multiple domains"
            description="My experience comes from active participation, leadership, self-learning, and building projects that reinforce technical fundamentals."
          />

          <div className="grid gap-6 md:grid-cols-2 xl:grid-cols-3">
            {experience.map((item) => {
              const Icon = item.icon;
              return (
                <Card key={item.title} className="rounded-[28px] border-white/10 bg-white/5">
                  <CardContent className="p-6">
                    <div className="flex items-start gap-4">
                      <div className="mt-1 flex h-11 w-11 shrink-0 items-center justify-center rounded-2xl bg-white/8 text-cyan-300">
                        <Icon className="h-5 w-5" />
                      </div>
                      <div>
                        <h3 className="text-lg font-semibold text-white">{item.title}</h3>
                        <p className="mt-2 text-sm leading-7 text-slate-300">{item.description}</p>
                      </div>
                    </div>
                  </CardContent>
                </Card>
              );
            })}
          </div>
        </motion.section>

        <motion.section
          initial="hidden"
          whileInView="visible"
          viewport={{ once: true, amount: 0.15 }}
          variants={fadeUp}
          transition={{ duration: 0.6, delay: 0.12 }}
          className="mt-24"
        >
          <SectionTitle
            eyebrow="Projects"
            title="Selected work"
            description="A few representative projects that reflect my current level, interests, and preferred way of learning by building."
          />

          <div className="grid gap-6 lg:grid-cols-2">
            {projects.map((project) => (
              <Card
                key={project.title}
                className={`rounded-[28px] border bg-white/5 ${project.featured ? "border-cyan-400/25" : "border-white/10"}`}
              >
                <CardContent className="p-7">
                  {project.featured ? (
                    <div className="mb-4 inline-flex rounded-full border border-cyan-400/20 bg-cyan-400/10 px-3 py-1 text-xs font-medium text-cyan-200">
                      Featured Project
                    </div>
                  ) : null}
                  <h3 className="text-xl font-semibold text-white">{project.title}</h3>
                  <p className="mt-3 text-sm leading-7 text-slate-300">{project.description}</p>
                  <div className="mt-5 flex flex-wrap gap-2">
                    {project.tags.map((tag) => (
                      <Badge key={tag} variant="secondary" className="border border-white/10 bg-white/5 text-slate-200">
                        {tag}
                      </Badge>
                    ))}
                  </div>
                  <div className="mt-6">
                    <a
                      href={project.link}
                      target="_blank"
                      rel="noreferrer"
                      className="inline-flex items-center gap-2 text-sm font-medium text-cyan-300 transition hover:text-cyan-200"
                    >
                      View Project <ExternalLink className="h-4 w-4" />
                    </a>
                  </div>
                </CardContent>
              </Card>
            ))}
          </div>
        </motion.section>

        <motion.section
          initial="hidden"
          whileInView="visible"
          viewport={{ once: true, amount: 0.2 }}
          variants={fadeUp}
          transition={{ duration: 0.6, delay: 0.14 }}
          className="mt-24"
        >
          <SectionTitle
            eyebrow="Skills"
            title="Technical stack"
            description="The tools and languages I currently use most in practice."
          />

          <div className="grid gap-6 lg:grid-cols-3">
            <SkillGroup title="Languages" items={skills.languages} />
            <SkillGroup title="Web" items={skills.web} />
            <SkillGroup title="Tools" items={skills.tools} />
          </div>
        </motion.section>

        <motion.section
          initial="hidden"
          whileInView="visible"
          viewport={{ once: true, amount: 0.2 }}
          variants={fadeUp}
          transition={{ duration: 0.6, delay: 0.16 }}
          className="mt-24"
        >
          <div className="grid gap-6 lg:grid-cols-2">
            <Card className="rounded-[28px] border-white/10 bg-white/5">
              <CardContent className="p-7">
                <h3 className="text-2xl font-bold text-white">Learning Approach</h3>
                <p className="mt-4 text-sm leading-8 text-slate-300 md:text-base">
                  I focus on practical learning through problem solving, competitions, and small but real projects. I believe hands-on work
                  builds deeper understanding than passive study alone, especially in fast-moving technical fields.
                </p>
              </CardContent>
            </Card>

            <Card className="rounded-[28px] border-white/10 bg-white/5">
              <CardContent className="p-7">
                <h3 className="text-2xl font-bold text-white">Goals</h3>
                <ul className="mt-4 space-y-3 text-sm text-slate-300 md:text-base">
                  {[
                    "Strengthen expertise in AI Engineering and Cybersecurity",
                    "Participate in higher-level international competitions",
                    "Join a strong technical team and contribute to real projects",
                  ].map((goal) => (
                    <li key={goal} className="flex items-start gap-3 leading-7">
                      <ChevronRight className="mt-1 h-4 w-4 shrink-0 text-cyan-400" />
                      <span>{goal}</span>
                    </li>
                  ))}
                </ul>
              </CardContent>
            </Card>
          </div>
        </motion.section>

        <motion.section
          initial="hidden"
          whileInView="visible"
          viewport={{ once: true, amount: 0.2 }}
          variants={fadeUp}
          transition={{ duration: 0.6, delay: 0.18 }}
          className="mt-24"
        >
          <Card className="overflow-hidden rounded-[32px] border border-cyan-400/20 bg-gradient-to-br from-cyan-500/10 via-slate-900 to-fuchsia-500/10">
            <CardContent className="p-8 md:p-10">
              <div className="flex flex-col gap-6 md:flex-row md:items-center md:justify-between">
                <div>
                  <p className="text-xs font-semibold uppercase tracking-[0.35em] text-cyan-300/80">Contact</p>
                  <h3 className="mt-3 text-3xl font-bold text-white">Let’s build something meaningful</h3>
                  <p className="mt-3 max-w-2xl text-sm leading-7 text-slate-300 md:text-base">
                    I am continuously learning, competing, and improving. If you want to connect around AI, cybersecurity, programming,
                    or technical collaboration, feel free to reach out.
                  </p>
                </div>
                <div className="flex flex-wrap gap-3">
                  <Button asChild size="lg" className="rounded-2xl bg-cyan-500 text-slate-950 hover:bg-cyan-400">
                    <a href="mailto:bayarbayasgalan.bb@gmail.com">
                      <Mail className="mr-2 h-4 w-4" />
                      Email Me
                    </a>
                  </Button>
                  <Button asChild size="lg" variant="outline" className="rounded-2xl border-white/15 bg-white/5 text-white hover:bg-white/10">
                    <a href="https://github.com/bebecpp" target="_blank" rel="noreferrer">
                      <Github className="mr-2 h-4 w-4" />
                      GitHub
                    </a>
                  </Button>
                </div>
              </div>
            </CardContent>
          </Card>
        </motion.section>
      </main>
    </div>
  );
}


![242390524-0c7eb6ed-663b-4ce4-bfbd-18239a38ba1b](https://github.com/user-attachments/assets/38dab773-a097-4865-a0ae-22dfc6608061)























     
![242390524-0c7eb6ed-663b-4ce4-bfbd-18239a38ba1b](https://github.com/user-attachments/assets/c479bbd2-9d24-4f94-9e9a-b489b1f12a77)
