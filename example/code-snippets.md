Visitor interface:

  internal interface IVisitor
  {
      void visit(Manager manager);
      void visit(Developer developer);
  }

Concrete Visitor:
      
    internal class AvrageSalaryCalaulatorVisitor : IVisitor
    {
        public void visit(Manager manager)
        {
            Console.WriteLine("This method calculates the avrage salary for Manager");
        }

        public void visit(Developer developer)
        {
            Console.WriteLine("This method calculates the avrage salary for Developer");
        }
    }

 Visitable Interface:

    
    internal interface IVisitable
    {
        void Accept(IVisitor visitor);
    }

  Application Objects:

        
    internal class Developer : IVisitable
    {
        public void Accept(IVisitor visitor)
        {
            visitor.visit(this);
        }
    }

    
    internal class Manager : IVisitable
    {
        public void Accept(IVisitor visitor)
        {
            visitor.visit(this);
        }
    }
      

    
    



