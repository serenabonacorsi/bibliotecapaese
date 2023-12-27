# bibliotecapaese
namespace Agenzia
{
    internal class Immobile
    {
        public string Codice { get; set; }
        public string Indirizzo { get; set; }
        public string Cap {  get; set; }
        public string Citta { get; set;}
        public int Superficie { get; set;}

        public Immobile(string codice, string indirizzo, string cap, string citta, int superficie)
        {
            Codice = codice;
            Indirizzo = indirizzo;
            Cap = Cap;
            Citta = Citta;
            Superficie = Superficie;
        }
        public override string ToString()
        {
            return string.Format("");
        }

        public void Dati()
        {
            return string.Format("Codice : {0}, Indirizzo : {1}, Cap : {2}, Citta : {3}, Superficie {4}", Codice , Indirizzo, Cap, Citta, Superficie, )
        }
    }
}
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Agenzia
{
    internal class Appartamento : Immobile
    {
        public int Numerovani { get; set; }
        public int Numerobagni { get; set; }

        public Appartamento(int Numerovani, int Numerobagni, string codice, string indirizzo, string cap, string citta, int superficie) : base(codice, indirizzo, cap, citta, superficie)
        {
            this.Numerovani = Numerovani;
            this.Numerobagni = Numerobagni;
        }

        public override string ToString()
        {
            return string.Format("il numero di Vani è di {0}, il numero di Bagni è di {1}", Numerovani, Numerobagni);
        }
    }
}
using System;
using System.Collections.Generic;
using System.Linq;
using System.Net.NetworkInformation;
using System.Text;
using System.Threading.Tasks;

namespace Agenzia
{
    internal class Box : Immobile
    {
        public int Postiauto { get; set; }
        public Box(string codice, string indirizzo, string cap, string citta, int superficie, int Postauto) : base(codice, indirizzo, cap, citta, superficie)
        {
            this.Postiauto = Postiauto;
        }
        public override string ToString()
        {
            return string.Format("Il numero di posti auto è di {0}", Postiauto);
        }
    }
}
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Agenzia
{
    internal class Villa
    {
        public int Giardino { get; set; }

        public Villa(int giardino, int Numerovani, int Numerobagni, string codice, string indirizzo, string cap, string citta, int superficie) : base(codice, indirizzo, cap, citta, superficie)
        {
            this.Giardino = giardino;
        }
        public override string ToString()
        {
            return string.Format("il giardino è di {0}", Giardino);
        }
    }
}

