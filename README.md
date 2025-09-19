# Apology-page
"use client"; import { motion } from "framer-motion"; import { Heart } from "lucide-react";

export default function Home() { return ( <main className="flex flex-col items-center justify-center min-h-screen bg-gradient-to-br from-pink-400 via-red-300 to-rose-500 text-white p-6 text-center"> {/* Floating hearts */} <div className="absolute inset-0 overflow-hidden pointer-events-none"> {[...Array(12)].map((_, i) => ( <motion.div key={i} initial={{ y: "100vh", opacity: 0 }} animate={{ y: ["100vh", "-10vh"], opacity: [0.2, 1, 0] }} transition={{ duration: 10 + i, repeat: Infinity, delay: i * 0.5 }} className="absolute left-[50%]" style={{ left: ${Math.random() * 100}% }} > <Heart className="w-6 h-6 text-pink-200" /> </motion.div> ))} </div>

{/* Main message */}
  <motion.h1
    initial={{ opacity: 0, scale: 0.8 }}
    animate={{ opacity: 1, scale: 1 }}
    transition={{ duration: 1 }}
    className="text-5xl md:text-7xl font-bold drop-shadow-lg mb-6"
  >
    I’m Sorry KuchuPuchu ❤️
  </motion.h1>

  <motion.p
    initial={{ opacity: 0 }}
    animate={{ opacity: 1 }}
    transition={{ delay: 1, duration: 1 }}
    className="text-lg md:text-2xl max-w-2xl leading-relaxed drop-shadow-md"
  >
    You mean the world to me. Please forgive me and let’s make more happy
    memories together 🌸
  </motion.p>

  <motion.button
    whileHover={{ scale: 1.1 }}
    whileTap={{ scale: 0.95 }}
    className="mt-8 bg-white text-pink-500 font-semibold px-6 py-3 rounded-2xl shadow-lg hover:bg-pink-100"
    onClick={() => alert("Love you forever ❤️")}
  >
    Tap to Forgive
  </motion.button>
</main>

); }

