import React, { useState, useEffect } from 'react';
import { 
  Zap, 
  Droplets, 
  ThermometerSnowflake, 
  Microscope,
  Phone, 
  Mail, 
  MapPin, 
  Menu, 
  X, 
  ArrowRight,
  ShieldCheck,
  Bug,
  ChevronRight,
  Sparkles,
  PhoneCall,
  Clock,
  Star,
  Plus,
  Minus,
  Award,
  Users,
  HardHat,
  CheckCircle,
  AlertCircle,
  TrendingUp,
  Zap as Lightning,
  Send
} from 'lucide-react';

const App = () => {
  const [isMobileMenuOpen, setIsMobileMenuOpen] = useState(false);
  const [formStatus, setFormStatus] = useState('idle');
  const [formData, setFormData] = useState({ projectType: '', requirements: '', name: '', phone: '' });
  const [openFaq, setOpenFaq] = useState(null);
  const [isScrolled, setIsScrolled] = useState(false);

  const primaryPhone = "+211927433947";
  const displayPhone = "+211 927 433 947";
  const emailAddress = "dabilicontracting@gmail.com";

  useEffect(() => {
    const handleScroll = () => setIsScrolled(window.scrollY > 50);
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  }, []);

  const handleFormChange = (e) => {
    const { name, value } = e.target;
    setFormData(prev => ({ ...prev, [name]: value }));
  };

  const handleFormSubmit = (e) => {
    e.preventDefault();
    if (!formData.projectType || !formData.requirements || !formData.name || !formData.phone) {
      alert('Please fill in all fields');
      return;
    }
    
    setFormStatus('submitting');
    
    // Simulate API call
    setTimeout(() => {
      setFormStatus('success');
      setFormData({ projectType: '', requirements: '', name: '', phone: '' });
      setTimeout(() => setFormStatus('idle'), 5000);
    }, 1500);
  };

  const scrollToSection = (id) => {
    const element = document.getElementById(id);
    if (element) {
      element.scrollIntoView({ behavior: 'smooth' });
    }
    setIsMobileMenuOpen(false);
  };

  const services = [
    { 
      icon: Zap, 
      title: 'Electrical Engineering', 
      desc: 'Expert industrial wiring, power system repairs, and backup generator maintenance.', 
      color: 'bg-yellow-100 text-yellow-700',
      details: ['Industrial Wiring', 'Power Systems', 'Generator Maintenance']
    },
    { 
      icon: Microscope, 
      title: 'Biomedical Equipment', 
      desc: 'High-precision calibration and maintenance for hospitals and clinical laboratories.', 
      color: 'bg-blue-50 text-blue-600',
      details: ['Equipment Calibration', 'Lab Support', 'Hospital Integration']
    },
    { 
      icon: Bug, 
      title: 'Fumigation & Pest Control', 
      desc: 'HSE-compliant sanitation and pest eradication for commercial and residential zones.', 
      color: 'bg-emerald-50 text-emerald-600',
      details: ['Pest Control', 'Sanitation', 'HSE Compliance']
    },
    { 
      icon: ThermometerSnowflake, 
      title: 'HVAC Services', 
      desc: 'AC installation, refrigeration repairs, and ventilation for high-heat environments.', 
      color: 'bg-sky-50 text-sky-600',
      details: ['AC Installation', 'Refrigeration', 'Ventilation']
    },
    { 
      icon: Droplets, 
      title: 'Plumbing Works', 
      desc: 'Pressure testing, sanitation piping, and general plumbing overhaul.', 
      color: 'bg-cyan-50 text-cyan-600',
      details: ['Pressure Testing', 'Sanitation Piping', 'Plumbing Repair']
    },
    { 
      icon: HardHat, 
      title: 'Civil Maintenance', 
      desc: 'General facility repairs, painting, and structural maintenance for buildings.', 
      color: 'bg-orange-50 text-orange-600',
      details: ['Facility Repairs', 'Painting', 'Structural Work']
    }
  ];

  const projects = [
    { title: "Hospital Lab Calibration", category: "Biomedical", img: "https://images.unsplash.com/photo-1579154236594-c199f346e7f7?auto=format&fit=crop&q=80&w=400", year: 2024 },
    { title: "Commercial HVAC Overhaul", category: "HVAC", img: "https://images.unsplash.com/photo-1504328345606-18bbc8c9d7d1?auto=format&fit=crop&q=80&w=400", year: 2024 },
    { title: "Industrial Wiring Project", category: "Electrical", img: "https://images.unsplash.com/photo-1621905251189-08b45d6a269e?auto=format&fit=crop&q=80&w=400", year: 2023 },
    { title: "Corporate Fumigation", category: "Sanitation", img: "https://images.unsplash.com/photo-1584622650111-993a426fbf0a?auto=format&fit=crop&q=80&w=400", year: 2023 },
  ];

  const testimonials = [
    { name: "Dr. Ahmed Hassan", role: "Hospital Director", text: "DABILI's biomedical expertise saved us thousands in equipment downtime. Professional, reliable, swift.", rating: 5 },
    { name: "Sarah Okonkwo", role: "Facility Manager", text: "24/7 response is no joke. They truly care about our operations.", rating: 5 },
    { name: "James Muwangira", role: "Plant Manager", text: "Best maintenance contractor in Juba. Certified staff, quality work.", rating: 5 },
  ];

  const stats = [
    { number: "500+", label: "Successful Projects" },
    { number: "24/7", label: "Emergency Response" },
    { number: "99.8%", label: "Uptime Rate" },
    { number: "20+", label: "Expert Engineers" },
  ];

  const faqs = [
    { q: "How fast is your emergency response?", a: "We aim for a 2-hour response time within Juba for critical electrical or biomedical failures. Emergency hotline available 24/7." },
    { q: "Are your technicians certified?", a: "Yes, all DABILI technicians are certified professionals in their respective engineering fields with ongoing training programs." },
    { q: "Do you offer annual maintenance contracts?", a: "We provide tailored Annual Maintenance Contracts (AMC) for corporate and medical facilities with flexible pricing and priority support." },
    { q: "Is your fumigation safe for hospitals?", a: "We use hospital-grade, non-toxic chemicals that are effective yet safe for sensitive environments. Full HSE compliance certified." },
    { q: "What areas do you service?", a: "We primarily serve Juba and surrounding regions. Contact us for specific location inquiries." },
    { q: "Do you provide spare parts?", a: "Yes, we stock genuine spare parts for major equipment and can source specialized components." }
  ];

  const Logo = ({ light = false }) => (
    <div className="flex items-center gap-2 cursor-pointer" onClick={() => window.scrollTo({top: 0, behavior: 'smooth'})}>
      <div className={`relative flex items-center justify-center w-10 h-10 border-2 rounded-full ${light ? 'border-white' : 'border-[#3a3633]'}`}>
        <Zap className={`h-6 w-6 ${light ? 'text-white' : 'text-[#3a3633]'}`} />
        <div className={`absolute -bottom-1 -right-1 w-3 h-3 rounded-full border-2 ${light ? 'bg-white border-[#3a3633]' : 'bg-[#3a3633] border-white'}`}></div>
      </div>
      <div className="flex flex-col leading-none">
        <span className={`font-black text-xl tracking-tighter ${light ? 'text-white' : 'text-[#3a3633]'}`}>DABILI</span>
        <span className={`text-[8px] font-bold tracking-[0.2em] uppercase ${light ? 'text-white/80' : 'text-[#3a3633]/80'}`}>Engineering</span>
      </div>
    </div>
  );

  return (
    <div className="font-sans text-[#3a3633] bg-white min-h-screen selection:bg-[#f3bc4c] selection:text-[#3a3633]">
      {/* Floating Action Call Button */}
      <div className="fixed bottom-6 right-6 z-[60] flex flex-col gap-3">
        <a 
          href={`tel:${primaryPhone}`} 
          className="bg-[#f3bc4c] text-[#3a3633] w-14 h-14 rounded-full flex items-center justify-center shadow-2xl hover:scale-110 transition-all border-4 border-white animate-pulse"
        >
          <PhoneCall className="h-6 w-6" />
        </a>
        <a 
          href={`mailto:${emailAddress}`}
          className="bg-[#3a3633] text-[#f3bc4c] w-14 h-14 rounded-full flex items-center justify-center shadow-2xl hover:scale-110 transition-all border-4 border-white"
        >
          <Mail className="h-6 w-6" />
        </a>
      </div>

      {/* Navigation */}
      <nav className={`fixed w-full z-50 transition-all duration-300 ${isScrolled ? 'bg-white/98 backdrop-blur-md shadow-lg' : 'bg-white/95 backdrop-blur-md'} border-b border-slate-100`}>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div className="flex justify-between h-20 items-center">
            <Logo />
            <div className="hidden md:flex items-center space-x-8">
              <button onClick={() => scrollToSection('services')} className="text-xs font-black uppercase tracking-widest hover:text-[#f3bc4c] transition-colors">Services</button>
              <button onClick={() => scrollToSection('projects')} className="text-xs font-black uppercase tracking-widest hover:text-[#f3bc4c] transition-colors">Portfolio</button>
              <button onClick={() => scrollToSection('about')} className="text-xs font-black uppercase tracking-widest hover:text-[#f3bc4c] transition-colors">The CEO</button>
              <button onClick={() => scrollToSection('testimonials')} className="text-xs font-black uppercase tracking-widest hover:text-[#f3bc4c] transition-colors">Testimonials</button>
              <button onClick={() => scrollToSection('contact')} className="bg-[#f3bc4c] text-[#3a3633] px-6 py-2.5 rounded font-black text-xs uppercase tracking-widest shadow-lg hover:shadow-xl hover:scale-105 transition-all">Request Service</button>
            </div>
            <button className="md:hidden p-2" onClick={() => setIsMobileMenuOpen(!isMobileMenuOpen)}>
              {isMobileMenuOpen ? <X /> : <Menu />}
            </button>
          </div>
        </div>
        {isMobileMenuOpen && (
          <div className="md:hidden bg-white border-t p-6 space-y-4 animate-in slide-in-from-top">
            <button onClick={() => scrollToSection('services')} className="block font-bold w-full text-left">Services</button>
            <button onClick={() => scrollToSection('projects')} className="block font-bold w-full text-left">Portfolio</button>
            <button onClick={() => scrollToSection('about')} className="block font-bold w-full text-left">The CEO</button>
            <button onClick={() => scrollToSection('testimonials')} className="block font-bold w-full text-left">Testimonials</button>
            <a href={`tel:${primaryPhone}`} className="flex items-center justify-center gap-2 w-full p-4 bg-[#3a3633] text-[#f3bc4c] rounded-lg font-black hover:bg-black transition-colors">
              <PhoneCall className="h-5 w-5" /> CALL NOW
            </a>
          </div>
        )}
      </nav>

      {/* Hero Section */}
      <section className="relative pt-32 pb-20 lg:pt-48 lg:pb-36 bg-gradient-to-br from-[#f3bc4c] to-[#ffd580]">
        <div className="absolute inset-0 overflow-hidden">
          <div className="absolute -top-40 -right-40 w-80 h-80 bg-white/10 rounded-full blur-3xl"></div>
          <div className="absolute -bottom-40 -left-40 w-80 h-80 bg-[#3a3633]/10 rounded-full blur-3xl"></div>
        </div>
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
          <div className="grid lg:grid-cols-2 gap-16 items-center">
            <div>
              <div className="inline-flex items-center gap-2 px-3 py-1 bg-[#3a3633] text-white text-[10px] font-black uppercase tracking-widest mb-6 rounded-full">
                <ShieldCheck className="h-3 w-3 text-[#f3bc4c]" /> Juba's Choice for Maintenance
              </div>
              <h1 className="text-6xl lg:text-8xl font-black text-[#3a3633] mb-8 leading-[0.9] tracking-tighter">
                WE KEEP <br/>IT RUNNING.
              </h1>
              <p className="text-xl text-[#3a3633]/80 mb-10 leading-relaxed font-medium">
                DABILI Engineering: Your dedicated partner for specialized maintenance in South Sudan. 24/7 emergency response, certified technicians, ISO-compliant operations.
              </p>
              <div className="flex flex-wrap gap-4">
                <button onClick={() => scrollToSection('contact')} className="bg-[#3a3633] text-white px-10 py-5 rounded font-black text-lg flex items-center gap-2 hover:bg-black transition-all hover:shadow-xl hover:scale-105">
                  Get a Quote <ArrowRight className="h-5 w-5 text-[#f3bc4c]" />
                </button>
                <div className="flex items-center gap-4 bg-white/30 p-4 rounded-lg backdrop-blur-sm border border-white/40 hover:bg-white/40 transition-all">
                  <div className="flex -space-x-2">
                    {[1,2,3].map(i => <div key={i} className="w-10 h-10 rounded-full border-2 border-white bg-slate-400 flex items-center justify-center text-[10px] font-black text-white">ENG</div>)}
                  </div>
                  <span className="text-sm font-black uppercase text-[#3a3633]">20+ Expert Staff</span>
                </div>
              </div>
            </div>
            <div className="hidden lg:block relative">
              <div className="grid grid-cols-2 gap-4">
                <img src="https://images.unsplash.com/photo-1504328345606-18bbc8c9d7d1?auto=format&fit=crop&q=80&w=400" className="rounded-2xl shadow-2xl mt-12 hover:scale-105 transition-transform" alt="HVAC Engineering" />
                <img src="https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?auto=format&fit=crop&q=80&w=400" className="rounded-2xl shadow-2xl hover:scale-105 transition-transform" alt="Technical Work" />
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Stats Bar */}
      <div className="bg-[#3a3633] py-12">
        <div className="max-w-7xl mx-auto px-4">
          <div className="grid grid-cols-2 md:grid-cols-4 gap-8">
            {stats.map((stat, i) => (
              <div key={i} className="text-center">
                <p className="text-4xl lg:text-5xl font-black text-[#f3bc4c] mb-2">{stat.number}</p>
                <p className="text-[10px] font-black uppercase tracking-widest text-slate-400">{stat.label}</p>
              </div>
            ))}
          </div>
        </div>
      </div>

      {/* Feature Trust Bar */}
      <div className="bg-slate-50 py-12 border-b border-slate-200">
        <div className="max-w-7xl mx-auto px-4">
          <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
            {[
              { icon: Clock, t: "24/7 Response", d: "Emergency Callouts" },
              { icon: Award, t: "ISO Standard", d: "Quality Compliance" },
              { icon: Users, t: "Dedicated Teams", d: "Bespoke Maintenance" }
            ].map((item, i) => (
              <div key={i} className="flex items-center gap-4 p-6 bg-white rounded-lg border border-slate-100 hover:border-[#f3bc4c] transition-all">
                <item.icon className="h-8 w-8 text-[#f3bc4c] flex-shrink-0" />
                <div>
                  <p className="font-black text-sm uppercase tracking-tighter text-[#3a3633]">{item.t}</p>
                  <p className="text-[10px] text-slate-400 font-bold uppercase tracking-widest">{item.d}</p>
                </div>
              </div>
            ))}
          </div>
        </div>
      </div>

      {/* Services Grid */}
      <section id="services" className="py-24 bg-white">
        <div className="max-w-7xl mx-auto px-4">
          <div className="mb-20">
            <h2 className="text-[#f3bc4c] font-black uppercase tracking-[0.3em] text-xs mb-4">What we do</h2>
            <h3 className="text-5xl font-black text-[#3a3633]">Engineering Expertise</h3>
            <p className="text-slate-500 mt-4 text-lg max-w-2xl">Six specialized services designed to keep your operations running smoothly, 24/7.</p>
          </div>
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            {services.map((s, i) => (
              <div key={i} className="group p-8 border-2 border-slate-100 hover:border-[#f3bc4c] transition-all bg-slate-50/50 hover:bg-white rounded-xl hover:shadow-xl">
                <div className={`w-12 h-12 flex items-center justify-center mb-6 ${s.color} rounded-lg group-hover:scale-110 transition-transform`}>
                  <s.icon className="h-6 w-6" />
                </div>
                <h4 className="text-xl font-black mb-3 text-[#3a3633]">{s.title}</h4>
                <p className="text-slate-500 font-medium text-sm leading-relaxed mb-6">{s.desc}</p>
                <div className="flex flex-wrap gap-2 mb-6">
                  {s.details.map((detail, j) => (
                    <span key={j} className="text-[9px] bg-slate-100 text-slate-600 px-2 py-1 rounded font-bold uppercase">{detail}</span>
                  ))}
                </div>
                <button onClick={() => scrollToSection('contact')} className="text-[10px] font-black uppercase tracking-widest text-[#3a3633] flex items-center gap-2 group-hover:text-[#f3bc4c] transition-colors">
                  Get Quote <ChevronRight className="h-3 w-3" />
                </button>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Project Portfolio */}
      <section id="projects" className="py-24 bg-slate-50">
        <div className="max-w-7xl mx-auto px-4">
          <div className="flex justify-between items-end mb-16">
            <div>
              <h2 className="text-[#f3bc4c] font-black tracking-widest uppercase text-xs mb-4">Portfolio</h2>
              <h3 className="text-5xl font-black text-[#3a3633]">Completed Works</h3>
            </div>
            <button onClick={() => scrollToSection('contact')} className="hidden md:block font-black text-xs uppercase tracking-widest text-[#f3bc4c] border-b-2 border-[#f3bc4c] hover:text-[#3a3633] transition-colors">View More</button>
          </div>
          <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
            {projects.map((p, i) => (
              <div key={i} className="group relative aspect-[3/4] overflow-hidden rounded-xl bg-[#3a3633] hover:shadow-2xl transition-all">
                <img src={p.img} alt={p.title} className="w-full h-full object-cover opacity-60 group-hover:scale-110 transition-transform duration-700" />
                <div className="absolute inset-0 bg-gradient-to-t from-black/60 to-transparent p-6 flex flex-col justify-end">
                  <div className="flex items-center justify-between mb-3">
                    <span className="text-[10px] font-black uppercase text-[#f3bc4c] tracking-widest bg-black/40 px-3 py-1 rounded-full">{p.category}</span>
                    <span className="text-[10px] font-black text-white/70">{p.year}</span>
                  </div>
                  <h5 className="text-white font-black text-lg leading-tight group-hover:text-[#f3bc4c] transition-colors">{p.title}</h5>
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Testimonials Section */}
      <section id="testimonials" className="py-24 bg-white">
        <div className="max-w-7xl mx-auto px-4">
          <div className="text-center mb-16">
            <h2 className="text-[#f3bc4c] font-black uppercase tracking-[0.3em] text-xs mb-4">Reviews</h2>
            <h3 className="text-5xl font-black text-[#3a3633]">What Clients Say</h3>
          </div>
          <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
            {testimonials.map((testimonial, i) => (
              <div key={i} className="p-8 bg-slate-50 rounded-xl border border-slate-100 hover:border-[#f3bc4c] transition-all hover:shadow-lg">
                <div className="flex gap-1 mb-4">
                  {[...Array(testimonial.rating)].map((_, j) => (
                    <Star key={j} className="h-4 w-4 fill-[#f3bc4c] text-[#f3bc4c]" />
                  ))}
                </div>
                <p className="text-slate-600 font-medium mb-6 leading-relaxed italic">"{testimonial.text}"</p>
                <div>
                  <p className="font-black text-[#3a3633]">{te
