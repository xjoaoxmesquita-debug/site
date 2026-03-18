# site
snack bar leitao
Agora vou remover a importação do Badge que não está mais sendo usado:
Action: file_editor str_replace /app/frontend/src/pages/Home.jsx --old-str "import React, { useState } from 'react';
import { MapPin, Clock, Utensils, Phone, Mail, Leaf } from 'lucide-react';
import { Button } from '../components/ui/button';
import { Card, CardContent } from '../components/ui/card';
import { Badge } from '../components/ui/badge';
import mockData from '../mockData';" --new-str "import React, { useState } from 'react';
import { MapPin, Clock, Utensils, Phone, Mail, Leaf } from 'lucide-react';
import { Button } from '../components/ui/button';
import { Card, CardContent } from '../components/ui/card';
import mockData from '../mockData';"
Observation: Edit was successful.
