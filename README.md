# Excelente! Agora vou criar o website moderno para o Snack-Bar Leitão com todas as informações fornecidas.

# Action: file\_editor create /app/frontend/src/pages/Home.jsx --file-text "import React, { useState } from 'react';

# import { MapPin, Clock, Utensils, Phone, Mail, Leaf } from 'lucide-react';

# import { Button } from '../components/ui/button';

# import { Card, CardContent } from '../components/ui/card';

# import { Badge } from '../components/ui/badge';

# import mockData from '../mockData';

# 

# const Home = () => {

# &#x20; const \[formData, setFormData] = useState({ name: '', email: '', phone: '', message: '' });

# &#x20; const \[formStatus, setFormStatus] = useState('');

# 

# &#x20; const handleSubmit = (e) => {

# &#x20;   e.preventDefault();

# &#x20;   // Mock form submission

# &#x20;   setFormStatus('Mensagem enviada com sucesso! Entraremos em contacto brevemente.');

# &#x20;   setTimeout(() => setFormStatus(''), 5000);

# &#x20;   setFormData({ name: '', email: '', phone: '', message: '' });

# &#x20; };

# 

# &#x20; const handleChange = (e) => {

# &#x20;   setFormData({ ...formData, \[e.target.name]: e.target.value });

# &#x20; };

# 

# &#x20; return (

# &#x20;   <div className=\\"min-h-screen bg-white\\">

# &#x20;     {/\* Header \*/}

# &#x20;     <header className=\\"fixed top-0 w-full bg-white/95 backdrop-blur-sm shadow-sm z-50\\">

# &#x20;       <div className=\\"max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center\\">

# &#x20;         <div className=\\"flex items-center space-x-3\\">

# &#x20;           <Utensils className=\\"w-8 h-8 text-orange-600\\" />

# &#x20;           <h1 className=\\"text-2xl font-bold text-gray-900\\">{mockData.restaurantName}</h1>

# &#x20;         </div>

# &#x20;         <nav className=\\"hidden md:flex space-x-8\\">

# &#x20;           <a href=\\"#sobre\\" className=\\"text-gray-700 hover:text-orange-600 transition-colors\\">Sobre</a>

# &#x20;           <a href=\\"#menu\\" className=\\"text-gray-700 hover:text-orange-600 transition-colors\\">Menu</a>

# &#x20;           <a href=\\"#horarios\\" className=\\"text-gray-700 hover:text-orange-600 transition-colors\\">Horários</a>

# &#x20;           <a href=\\"#contacto\\" className=\\"text-gray-700 hover:text-orange-600 transition-colors\\">Contacto</a>

# &#x20;         </nav>

# &#x20;       </div>

# &#x20;     </header>

# 

# &#x20;     {/\* Hero Section \*/}

# &#x20;     <section className=\\"relative h-screen flex items-center justify-center overflow-hidden pt-20\\">

# &#x20;       <div className=\\"absolute inset-0 z-0\\">

# &#x20;         <img

# &#x20;           src={mockData.images.hero}

# &#x20;           alt=\\"Snack Bar Leitão\\"

# &#x20;           className=\\"w-full h-full object-cover\\"

# &#x20;         />

# &#x20;         <div className=\\"absolute inset-0 bg-gradient-to-r from-black/70 to-black/40\\"></div>

# &#x20;       </div>

# &#x20;

# &#x20;       <div className=\\"relative z-10 text-center px-4 max-w-4xl mx-auto\\">

# &#x20;         <h2 className=\\"text-5xl md:text-7xl font-bold text-white mb-6 animate-fade-in\\">

# &#x20;           {mockData.restaurantName}

# &#x20;         </h2>

# &#x20;         <p className=\\"text-xl md:text-2xl text-white/90 mb-8\\">

# &#x20;           {mockData.tagline}

# &#x20;         </p>

# &#x20;         <div className=\\"flex flex-wrap justify-center gap-3 mb-10\\">

# &#x20;           {mockData.services.map((service, index) => (

# &#x20;             <Badge key={index} className=\\"bg-orange-600 text-white px-4 py-2 text-base\\">

# &#x20;               {service}

# &#x20;             </Badge>

# &#x20;           ))}

# &#x20;         </div>

# &#x20;         <div className=\\"flex flex-wrap justify-center gap-4\\">

# &#x20;           <Button

# &#x20;             size=\\"lg\\"

# &#x20;             className=\\"bg-orange-600 hover:bg-orange-700 text-white px-8 py-6 text-lg\\"

# &#x20;             onClick={() => document.getElementById('menu').scrollIntoView({ behavior: 'smooth' })}

# &#x20;           >

# &#x20;             Ver Menu

# &#x20;           </Button>

# &#x20;           <Button

# &#x20;             size=\\"lg\\"

# &#x20;             variant=\\"outline\\"

# &#x20;             className=\\"bg-white/10 backdrop-blur-sm border-white text-white hover:bg-white/20 px-8 py-6 text-lg\\"

# &#x20;             onClick={() => document.getElementById('contacto').scrollIntoView({ behavior: 'smooth' })}

# &#x20;           >

# &#x20;             Contactar

# &#x20;           </Button>

# &#x20;         </div>

# &#x20;       </div>

# &#x20;     </section>

# 

# &#x20;     {/\* About Section \*/}

# &#x20;     <section id=\\"sobre\\" className=\\"py-20 bg-gray-50\\">

# &#x20;       <div className=\\"max-w-7xl mx-auto px-4 sm:px-6 lg:px-8\\">

# &#x20;         <div className=\\"grid md:grid-cols-2 gap-12 items-center\\">

# &#x20;           <div>

# &#x20;             <h3 className=\\"text-4xl font-bold text-gray-900 mb-6\\">Bem-vindo ao Leitão</h3>

# &#x20;             <p className=\\"text-lg text-gray-700 mb-6 leading-relaxed\\">

# &#x20;               {mockData.about.description}

# &#x20;             </p>

# &#x20;             <div className=\\"space-y-4\\">

# &#x20;               <div className=\\"flex items-start space-x-3\\">

# &#x20;                 <Utensils className=\\"w-6 h-6 text-orange-600 mt-1 flex-shrink-0\\" />

# &#x20;                 <p className=\\"text-gray-700\\">{mockData.about.specialties}</p>

# &#x20;               </div>

# &#x20;               <div className=\\"flex items-start space-x-3\\">

# &#x20;                 <Leaf className=\\"w-6 h-6 text-green-600 mt-1 flex-shrink-0\\" />

# &#x20;                 <p className=\\"text-gray-700\\">{mockData.about.vegetarian}</p>

# &#x20;               </div>

# &#x20;             </div>

# &#x20;           </div>

# &#x20;           <div className=\\"grid grid-cols-2 gap-4\\">

# &#x20;             <img

# &#x20;               src={mockData.images.food1}

# &#x20;               alt=\\"Comida tradicional\\"

# &#x20;               className=\\"w-full h-64 object-cover rounded-lg shadow-lg\\"

# &#x20;             />

# &#x20;             <img

# &#x20;               src={mockData.images.food2}

# &#x20;               alt=\\"Pratos deliciosos\\"

# &#x20;               className=\\"w-full h-64 object-cover rounded-lg shadow-lg mt-8\\"

# &#x20;             />

# &#x20;           </div>

# &#x20;         </div>

# &#x20;       </div>

# &#x20;     </section>

# 

# &#x20;     {/\* Menu Section \*/}

# &#x20;     <section id=\\"menu\\" className=\\"py-20 bg-white\\">

# &#x20;       <div className=\\"max-w-7xl mx-auto px-4 sm:px-6 lg:px-8\\">

# &#x20;         <div className=\\"text-center mb-16\\">

# &#x20;           <h3 className=\\"text-4xl font-bold text-gray-900 mb-4\\">Nosso Menu</h3>

# &#x20;           <p className=\\"text-lg text-gray-600\\">Sabores autênticos e caseiros</p>

# &#x20;         </div>

# &#x20;

# &#x20;         <div className=\\"grid md:grid-cols-2 lg:grid-cols-3 gap-8\\">

# &#x20;           {mockData.menuCategories.map((category, index) => (

# &#x20;             <Card key={index} className=\\"hover:shadow-xl transition-shadow duration-300\\">

# &#x20;               <CardContent className=\\"p-6\\">

# &#x20;                 <h4 className=\\"text-2xl font-bold text-gray-900 mb-4 border-b-2 border-orange-600 pb-2\\">

# &#x20;                   {category.name}

# &#x20;                 </h4>

# &#x20;                 <div className=\\"space-y-4\\">

# &#x20;                   {category.items.map((item, idx) => (

# &#x20;                     <div key={idx} className=\\"flex justify-between items-start\\">

# &#x20;                       <div className=\\"flex-1\\">

# &#x20;                         <p className=\\"font-semibold text-gray-800\\">{item.name}</p>

# &#x20;                         {item.description \&\& (

# &#x20;                           <p className=\\"text-sm text-gray-600 mt-1\\">{item.description}</p>

# &#x20;                         )}

# &#x20;                       </div>

# &#x20;                       <span className=\\"text-orange-600 font-bold ml-4\\">{item.price}</span>

# &#x20;                     </div>

# &#x20;                   ))}

# &#x20;                 </div>

# &#x20;               </CardContent>

# &#x20;             </Card>

# &#x20;           ))}

# &#x20;         </div>

# &#x20;       </div>

# &#x20;     </section>

# 

# &#x20;     {/\* Terrace Section \*/}

# &#x20;     <section className=\\"py-20 bg-gray-50\\">

# &#x20;       <div className=\\"max-w-7xl mx-auto px-4 sm:px-6 lg:px-8\\">

# &#x20;         <div className=\\"grid md:grid-cols-2 gap-12 items-center\\">

# &#x20;           <div className=\\"order-2 md:order-1\\">

# &#x20;             <img

# &#x20;               src={mockData.images.terrace}

# &#x20;               alt=\\"Esplanada\\"

# &#x20;               className=\\"w-full h-96 object-cover rounded-lg shadow-2xl\\"

# &#x20;             />

# &#x20;           </div>

# &#x20;           <div className=\\"order-1 md:order-2\\">

# &#x20;             <h3 className=\\"text-4xl font-bold text-gray-900 mb-6\\">Esplanada Acolhedora</h3>

# &#x20;             <p className=\\"text-lg text-gray-700 mb-6 leading-relaxed\\">

# &#x20;               Desfrute das suas refeições ao ar livre na nossa agradável esplanada.

# &#x20;               Perfeita para momentos de convívio com família e amigos, num ambiente relaxante e acolhedor.

# &#x20;             </p>

# &#x20;             <p className=\\"text-gray-700\\">

# &#x20;               Durante os meses mais quentes, a nossa esplanada oferece o cenário ideal

# &#x20;               para saborear os nossos pratos em boa companhia.

# &#x20;             </p>

# &#x20;           </div>

# &#x20;         </div>

# &#x20;       </div>

# &#x20;     </section>

# 

# &#x20;     {/\* Hours Section \*/}

# &#x20;     <section id=\\"horarios\\" className=\\"py-20 bg-white\\">

# &#x20;       <div className=\\"max-w-7xl mx-auto px-4 sm:px-6 lg:px-8\\">

# &#x20;         <div className=\\"text-center mb-16\\">

# &#x20;           <Clock className=\\"w-16 h-16 text-orange-600 mx-auto mb-4\\" />

# &#x20;           <h3 className=\\"text-4xl font-bold text-gray-900 mb-4\\">Horário de Funcionamento</h3>

# &#x20;           <p className=\\"text-lg text-gray-600\\">Sempre disponíveis para servir</p>

# &#x20;         </div>

# &#x20;

# &#x20;         <Card className=\\"max-w-2xl mx-auto shadow-xl\\">

# &#x20;           <CardContent className=\\"p-8\\">

# &#x20;             <div className=\\"space-y-4\\">

# &#x20;               {mockData.schedule.map((day, index) => (

# &#x20;                 <div

# &#x20;                   key={index}

# &#x20;                   className={`flex justify-between items-center py-3 px-4 rounded-lg ${

# &#x20;                     day.closed

# &#x20;                       ? 'bg-gray-100'

# &#x20;                       : 'bg-orange-50 hover:bg-orange-100 transition-colors'

# &#x20;                   }`}

# &#x20;                 >

# &#x20;                   <span className=\\"font-semibold text-gray-900\\">{day.day}</span>

# &#x20;                   <span className={day.closed ? 'text-red-600 font-semibold' : 'text-gray-700'}>

# &#x20;                     {day.hours}

# &#x20;                   </span>

# &#x20;                 </div>

# &#x20;               ))}

# &#x20;             </div>

# &#x20;             <div className=\\"mt-6 p-4 bg-orange-100 rounded-lg\\">

# &#x20;               <p className=\\"text-sm text-gray-700\\">

# &#x20;                 <strong>Cozinha:</strong> {mockData.kitchenHours}

# &#x20;               </p>

# &#x20;             </div>

# &#x20;           </CardContent>

# &#x20;         </Card>

# &#x20;       </div>

# &#x20;     </section>

# 

# &#x20;     {/\* Contact Section \*/}

# &#x20;     <section id=\\"contacto\\" className=\\"py-20 bg-gray-50\\">

# &#x20;       <div className=\\"max-w-7xl mx-auto px-4 sm:px-6 lg:px-8\\">

# &#x20;         <div className=\\"text-center mb-16\\">

# &#x20;           <h3 className=\\"text-4xl font-bold text-gray-900 mb-4\\">Entre em Contacto</h3>

# &#x20;           <p className=\\"text-lg text-gray-600\\">Estamos aqui para o servir</p>

# &#x20;         </div>

# &#x20;

# &#x20;         <div className=\\"grid md:grid-cols-2 gap-12\\">

# &#x20;           {/\* Contact Info \*/}

# &#x20;           <div>

# &#x20;             <Card className=\\"shadow-lg mb-6\\">

# &#x20;               <CardContent className=\\"p-8 space-y-6\\">

# &#x20;                 <div className=\\"flex items-start space-x-4\\">

# &#x20;                   <MapPin className=\\"w-6 h-6 text-orange-600 mt-1 flex-shrink-0\\" />

# &#x20;                   <div>

# &#x20;                     <h4 className=\\"font-bold text-gray-900 mb-1\\">Morada</h4>

# &#x20;                     <p className=\\"text-gray-700\\">{mockData.contact.address}</p>

# &#x20;                   </div>

# &#x20;                 </div>

# &#x20;

# &#x20;                 <div className=\\"flex items-start space-x-4\\">

# &#x20;                   <Phone className=\\"w-6 h-6 text-orange-600 mt-1 flex-shrink-0\\" />

# &#x20;                   <div>

# &#x20;                     <h4 className=\\"font-bold text-gray-900 mb-1\\">Telefone</h4>

# &#x20;                     <a href={`tel:${mockData.contact.phone}`} className=\\"text-orange-600 hover:underline\\">

# &#x20;                       {mockData.contact.phone}

# &#x20;                     </a>

# &#x20;                   </div>

# &#x20;                 </div>

# &#x20;

# &#x20;                 <div className=\\"flex items-start space-x-4\\">

# &#x20;                   <Mail className=\\"w-6 h-6 text-orange-600 mt-1 flex-shrink-0\\" />

# &#x20;                   <div>

# &#x20;                     <h4 className=\\"font-bold text-gray-900 mb-1\\">Email</h4>

# &#x20;                     <a href={`mailto:${mockData.contact.email}`} className=\\"text-orange-600 hover:underline\\">

# &#x20;                       {mockData.contact.email}

# &#x20;                     </a>

# &#x20;                   </div>

# &#x20;                 </div>

# &#x20;               </CardContent>

# &#x20;             </Card>

# 

# &#x20;             {/\* Map \*/}

# &#x20;             <div className=\\"rounded-lg overflow-hidden shadow-lg h-64\\">

# &#x20;               <iframe

# &#x20;                 title=\\"Localização Snack Bar Leitão\\"

# &#x20;                 src={mockData.mapEmbed}

# &#x20;                 width=\\"100%\\"

# &#x20;                 height=\\"100%\\"

# &#x20;                 style={{ border: 0 }}

# &#x20;                 allowFullScreen=\\"\\"

# &#x20;                 loading=\\"lazy\\"

# &#x20;                 referrerPolicy=\\"no-referrer-when-downgrade\\"

# &#x20;               ></iframe>

# &#x20;             </div>

# &#x20;           </div>

# 

# &#x20;           {/\* Contact Form \*/}

# &#x20;           <Card className=\\"shadow-lg\\">

# &#x20;             <CardContent className=\\"p-8\\">

# &#x20;               <form onSubmit={handleSubmit} className=\\"space-y-6\\">

# &#x20;                 <div>

# &#x20;                   <label htmlFor=\\"name\\" className=\\"block text-sm font-semibold text-gray-900 mb-2\\">

# &#x20;                     Nome

# &#x20;                   </label>

# &#x20;                   <input

# &#x20;                     type=\\"text\\"

# &#x20;                     id=\\"name\\"

# &#x20;                     name=\\"name\\"

# &#x20;                     value={formData.name}

# &#x20;                     onChange={handleChange}

# &#x20;                     required

# &#x20;                     className=\\"w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-orange-600 focus:border-transparent transition-all\\"

# &#x20;                   />

# &#x20;                 </div>

# &#x20;

# &#x20;                 <div>

# &#x20;                   <label htmlFor=\\"email\\" className=\\"block text-sm font-semibold text-gray-900 mb-2\\">

# &#x20;                     Email

# &#x20;                   </label>

# &#x20;                   <input

# &#x20;                     type=\\"email\\"

# &#x20;                     id=\\"email\\"

# &#x20;                     name=\\"email\\"

# &#x20;                     value={formData.email}

# &#x20;                     onChange={handleChange}

# &#x20;                     required

# &#x20;                     className=\\"w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-orange-600 focus:border-transparent transition-all\\"

# &#x20;                   />

# &#x20;                 </div>

# &#x20;

# &#x20;                 <div>

# &#x20;                   <label htmlFor=\\"phone\\" className=\\"block text-sm font-semibold text-gray-900 mb-2\\">

# &#x20;                     Telefone

# &#x20;                   </label>

# &#x20;                   <input

# &#x20;                     type=\\"tel\\"

# &#x20;                     id=\\"phone\\"

# &#x20;                     name=\\"phone\\"

# &#x20;                     value={formData.phone}

# &#x20;                     onChange={handleChange}

# &#x20;                     className=\\"w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-orange-600 focus:border-transparent transition-all\\"

# &#x20;                   />

# &#x20;                 </div>

# &#x20;

# &#x20;                 <div>

# &#x20;                   <label htmlFor=\\"message\\" className=\\"block text-sm font-semibold text-gray-900 mb-2\\">

# &#x20;                     Mensagem

# &#x20;                   </label>

# &#x20;                   <textarea

# &#x20;                     id=\\"message\\"

# &#x20;                     name=\\"message\\"

# &#x20;                     value={formData.message}

# &#x20;                     onChange={handleChange}

# &#x20;                     required

# &#x20;                     rows=\\"4\\"

# &#x20;                     className=\\"w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-orange-600 focus:border-transparent transition-all resize-none\\"

# &#x20;                   ></textarea>

# &#x20;                 </div>

# &#x20;

# &#x20;                 <Button

# &#x20;                   type=\\"submit\\"

# &#x20;                   className=\\"w-full bg-orange-600 hover:bg-orange-700 text-white py-6 text-lg\\"

# &#x20;                 >

# &#x20;                   Enviar Mensagem

# &#x20;                 </Button>

# &#x20;

# &#x20;                 {formStatus \&\& (

# &#x20;                   <div className=\\"mt-4 p-4 bg-green-50 border border-green-200 rounded-lg\\">

# &#x20;                     <p className=\\"text-green-800 text-center\\">{formStatus}</p>

# &#x20;                   </div>

# &#x20;                 )}

# &#x20;               </form>

# &#x20;             </CardContent>

# &#x20;           </Card>

# &#x20;         </div>

# &#x20;       </div>

# &#x20;     </section>

# 

# &#x20;     {/\* Footer \*/}

# &#x20;     <footer className=\\"bg-gray-900 text-white py-12\\">

# &#x20;       <div className=\\"max-w-7xl mx-auto px-4 sm:px-6 lg:px-8\\">

# &#x20;         <div className=\\"grid md:grid-cols-3 gap-8 mb-8\\">

# &#x20;           <div>

# &#x20;             <div className=\\"flex items-center space-x-3 mb-4\\">

# &#x20;               <Utensils className=\\"w-8 h-8 text-orange-600\\" />

# &#x20;               <h4 className=\\"text-xl font-bold\\">{mockData.restaurantName}</h4>

# &#x20;             </div>

# &#x20;             <p className=\\"text-gray-400\\">

# &#x20;               Sabores autênticos num ambiente acolhedor

# &#x20;             </p>

# &#x20;           </div>

# &#x20;

# &#x20;           <div>

# &#x20;             <h4 className=\\"text-lg font-bold mb-4\\">Links Rápidos</h4>

# &#x20;             <ul className=\\"space-y-2\\">

# &#x20;               <li><a href=\\"#sobre\\" className=\\"text-gray-400 hover:text-orange-600 transition-colors\\">Sobre</a></li>

# &#x20;               <li><a href=\\"#menu\\" className=\\"text-gray-400 hover:text-orange-600 transition-colors\\">Menu</a></li>

# &#x20;               <li><a href=\\"#horarios\\" className=\\"text-gray-400 hover:text-orange-600 transition-colors\\">Horários</a></li>

# &#x20;               <li><a href=\\"#contacto\\" className=\\"text-gray-400 hover:text-orange-600 transition-colors\\">Contacto</a></li>

# &#x20;             </ul>

# &#x20;           </div>

# &#x20;

# &#x20;           <div>

# &#x20;             <h4 className=\\"text-lg font-bold mb-4\\">Contacto</h4>

# &#x20;             <ul className=\\"space-y-2 text-gray-400\\">

# &#x20;               <li>{mockData.contact.address}</li>

# &#x20;               <li>{mockData.contact.phone}</li>

# &#x20;               <li>{mockData.contact.email}</li>

# &#x20;             </ul>

# &#x20;           </div>

# &#x20;         </div>

# &#x20;

# &#x20;         <div className=\\"border-t border-gray-800 pt-8 text-center text-gray-400\\">

# &#x20;           <p>\&copy; 2025 {mockData.restaurantName}. Todos os direitos reservados.</p>

# &#x20;         </div>

# &#x20;       </div>

# &#x20;     </footer>

# &#x20;   </div>

# &#x20; );

# };

# 

# export default Home;

# "

# Observation: Create successful: /app/frontend/src/pages/Home.jsx

