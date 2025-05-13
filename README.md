import React from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { ShoppingCart, Phone, Info } from "lucide-react";

export default function EsleysElectronics() { const products = [ { name: "Multimeter", price: "$29.99", description: "Digital multimeter for precise measurements." }, { name: "Soldering Iron", price: "$19.99", description: "60W soldering iron with temperature control." }, { name: "Arduino Uno", price: "$24.99", description: "Microcontroller board for electronics projects." }, { name: "Oscilloscope", price: "$199.99", description: "Portable digital oscilloscope with LCD display." } ];

return ( <div className="p-6 space-y-8"> <header className="text-center space-y-2"> <h1 className="text-4xl font-bold">Esleys Electronics</h1> <p className="text-lg text-gray-600">Your one-stop shop for all electronics components and tools</p> </header>

<section className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
    {products.map((product, index) => (
      <Card key={index} className="rounded-2xl shadow-md">
        <CardContent className="p-4 space-y-2">
          <h2 className="text-xl font-semibold">{product.name}</h2>
          <p className="text-sm text-gray-500">{product.description}</p>
          <p className="text-lg font-bold">{product.price}</p>
          <Button className="w-full"><ShoppingCart className="mr-2" /> Add to Cart</Button>
        </CardContent>
      </Card>
    ))}
  </section>

  <footer className="text-center mt-10 space-y-2 text-gray-500">
    <p className="flex justify-center items-center gap-2"><Phone size={16} /> +1 (800) 123-4567</p>
    <p className="flex justify-center items-center gap-2"><Info size={16} /> info@esleyselectronics.com</p>
    <p>&copy; 2025 Esleys Electronics. All rights reserved.</p>
  </footer>
</div>

); }

