import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Download } from "lucide-react";
import { motion } from "framer-motion";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-slate-50 text-slate-900">
      {/* HERO */}
      <section className="bg-slate-900 text-white py-20 px-6">
        <div className="max-w-6xl mx-auto">
          <motion.h1 initial={{ opacity: 0, y: 20 }} animate={{ opacity: 1, y: 0 }} className="text-4xl font-bold">
            Norman Banda
          </motion.h1>
          <p className="mt-4 text-lg max-w-3xl">
            Senior programme and systems leader with 7+ years’ experience designing, funding, and delivering national-scale inclusion, governance, and youth-led programmes in Zambia.
          </p>
          <div className="mt-6 flex gap-4">
            <Button className="flex gap-2"><Download size={16}/> Download CV</Button>
            <Button variant="outline" className="flex gap-2"><Download size={16}/> Cover Letter</Button>
          </div>
        </div>
      </section>

      {/* LEADERSHIP PHILOSOPHY – RESTLESS VERSION */}
      <section className="py-16 px-6 max-w-6xl mx-auto">
        <h2 className="text-2xl font-bold mb-4">Leadership Philosophy – Youth-Led Development</h2>
        <p className="max-w-4xl mb-4">
          My leadership is grounded in the belief that young people are not beneficiaries of development, but powerful actors capable of shaping systems and solutions. I work to shift power, resources, and decision-making closer to young people and communities, embedding accountability, learning, and inclusion into institutions that serve them.
        </p>
        <p className="max-w-4xl">
          I prioritise locally led design, adaptive learning, and partnerships with government and civil society to ensure youth-led solutions are scalable, sustainable, and embedded within public systems—values closely aligned with Restless Development’s approach.
        </p>
      </section>

      {/* LEADERSHIP PHILOSOPHY – MENTAL HEALTH FOCUS */}
      <section className="bg-slate-100 py-16 px-6">
        <div className="max-w-6xl mx-auto">
          <h2 className="text-2xl font-bold mb-4">Leadership Philosophy – Mental Health & Wellbeing</h2>
          <p className="max-w-4xl">
            I approach mental health as both a public health and systems challenge. Sustainable impact requires integrating community-based, evidence-driven mental health services into existing government and social systems, while centring dignity, cultural relevance, and access for those most excluded.
          </p>
          <p className="max-w-4xl mt-3">
            My leadership focuses on enabling scale through partnerships, data-informed decision-making, safeguarding, and quality assurance—ensuring mental health interventions deliver measurable outcomes while strengthening national systems.
          </p>
        </div>
      </section>

      {/* IMPACT METRICS */}
      <section className="bg-white py-16 px-6">
        <div className="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-6">
          {["8 Political Parties Engaged", "40% Org Funding Generated", "120+ Leaders Trained"].map((item) => (
            <Card key={item} className="rounded-2xl shadow">
              <CardContent className="p-6 text-center font-semibold">{item}</CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* EXPERIENCE */}
      <section className="py-16 px-6 max-w-6xl mx-auto">
        <h2 className="text-2xl font-bold mb-6">Professional Experience</h2>
        <div className="grid md:grid-cols-2 gap-6">
          <Card className="rounded-2xl shadow">
            <CardContent className="p-6">
              <h3 className="font-bold">Executive Director – CYLA</h3>
              <p className="text-sm text-slate-600">2025–Present</p>
              <ul className="list-disc ml-5 mt-3">
                <li>Organisational leadership, governance, compliance, and partnerships</li>
                <li>Women and Girls Fund proposal shortlisted</li>
              </ul>
            </CardContent>
          </Card>
          <Card className="rounded-2xl shadow">
            <CardContent className="p-6">
              <h3 className="font-bold">Project Manager – ZNWL</h3>
              <p className="text-sm text-slate-600">2020–2025</p>
              <ul className="list-disc ml-5 mt-3">
                <li>Led national inclusion and governance programmes</li>
                <li>Projects generated ~40% of annual organisational funding</li>
              </ul>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* PUBLICATIONS & POLICY */}
      <section className="bg-slate-100 py-16 px-6">
        <div className="max-w-6xl mx-auto">
          <h2 className="text-2xl font-bold mb-4">Publications & Policy Work</h2>
          <ul className="list-disc ml-6">
            <li>Research Paper: Disability and Higher Education – University of Zambia</li>
            <li>Position Paper on Mixed Member Electoral Systems (MMES)</li>
            <li>Technical inputs to constitutional and political inclusion reforms</li>
          </ul>
        </div>
      </section>

      {/* SPEAKING & FACILITATION */}
      <section className="bg-white py-16 px-6">
        <div className="max-w-6xl mx-auto">
          <h2 className="text-2xl font-bold mb-6">Speaking & Facilitation</h2>
          <p className="max-w-4xl mb-6">
            I am an experienced facilitator and speaker on inclusion, youth leadership, disability equality, gender-transformative programming, and systems change. I regularly design and deliver sessions for political parties, civil society organisations, media professionals, and youth leaders at national and sub-national level.
          </p>
          <ul className="list-disc ml-6">
            <li>Disability Equality & Inclusive Governance – 120+ political party representatives trained</li>
            <li>Gender-transformative approaches for media and electoral actors</li>
            <li>Youth leadership, safeguarding, and participation in public decision-making</li>
            <li>Facilitation of policy dialogues, technical working groups, and stakeholder consultations</li>
          </ul>
        </div>
      </section>

      {/* PARTNERS */}
      <section className="py-16 px-6 max-w-6xl mx-auto">
        <h2 className="text-2xl font-bold mb-6">Partners & Collaborators</h2>
        <div className="grid grid-cols-2 md:grid-cols-5 gap-6 items-center">
          <img src="/logos/znwl.png" alt="ZNWL" className="mx-auto h-16" />
          <img src="/logos/ndi.png" alt="NDI" className="mx-auto h-16" />
          <img src="/logos/demo-finland.png" alt="Demo Finland" className="mx-auto h-16" />
          <img src="/logos/un-trust-fund.png" alt="UN Trust Fund" className="mx-auto h-16" />
          <img src="/logos/cyla.png" alt="CYLA" className="mx-auto h-16" />
        </div>
      </section>

      {/* FOOTER */}
      <footer className="bg-slate-900 text-white py-8 text-center">
        © 2026 Norman Banda | Youth-Led Systems Leadership
      </footer>
    </div>
  );
}
