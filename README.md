# Loja-de-ebook- 
https://wa.me/5581987176081?text=Ol%C3%A1!%20Quero%20comprar%20o%20eBook%20de%20reda%C3%A7%C3%A3o
import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Input } from "@/components/ui/input"; import { Mail } from "lucide-react";

export default function LojaEbook() { const whatsappLink = "https://wa.me/5581987176081?text=Ol%C3%A1!%20Quero%20comprar%20o%20eBook%20de%20reda%C3%A7%C3%A3o.";

return ( <div className="p-6 space-y-12"> {/* Início */} <section className="text-center space-y-4"> <h1 className="text-4xl font-bold">Loja de eBooks de Redação</h1> <p className="text-lg text-gray-600 max-w-xl mx-auto"> Aprimore suas habilidades de redação com nossos eBooks completos e atualizados para o ENEM e vestibulares. </p> <Button className="text-lg px-6 py-4" asChild> <a href="#produtos">Ver eBooks</a> </Button> </section>

{/* Sobre */}
  <section className="space-y-2">
    <h2 className="text-2xl font-semibold">Sobre Nós</h2>
    <p className="text-gray-700 max-w-2xl">
      Somos uma equipe apaixonada por educação que acredita que todos podem alcançar notas incríveis em redação com a orientação certa. Nossos eBooks são escritos por especialistas e trazem temas, repertórios, modelos prontos e análises nota 1000.
    </p>
  </section>

  {/* Produtos */}
  <section id="produtos" className="space-y-4">
    <h2 className="text-2xl font-semibold">Nossos eBooks</h2>
    <div className="grid grid-cols-1 md:grid-cols-3 gap-6">
      {[1, 2, 3].map((i) => (
        <Card key={i} className="rounded-2xl shadow-md">
          <CardContent className="p-4 space-y-2">
            <h3 className="text-lg font-bold">eBook Redação {i}</h3>
            <p className="text-sm text-gray-600">Conteúdo atualizado + dicas + temas inéditos.</p>
            <Button asChild>
              <a href={whatsappLink} target="_blank" rel="noopener noreferrer">
                Comprar via WhatsApp
              </a>
            </Button>
          </CardContent>
        </Card>
      ))}
    </div>
  </section>

  {/* Contato */}
  <section className="space-y-4">
    <h2 className="text-2xl font-semibold">Fale com a gente</h2>
    <div className="max-w-md space-y-2">
      <label className="block text-sm font-medium">Seu email</label>
      <Input type="email" placeholder="seu@email.com" />
      <label className="block text-sm font-medium">Mensagem</label>
      <Input type="text" placeholder="Escreva sua dúvida ou sugestão" />
      <Button className="mt-2 flex items-center gap-2">
        <Mail size={16} /> Enviar
      </Button>
    </div>
  </section>
</div>

); }

