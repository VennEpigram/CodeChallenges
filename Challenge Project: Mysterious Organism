// Returns a random DNA base
const returnRandBase = () => {
  const dnaBases = ['A', 'T', 'C', 'G']
  return dnaBases[Math.floor(Math.random() * 4)] 
}

// Returns a random single strand of DNA containing 15 bases
const mockUpStrand = () => {
  const newStrand = []
  for (let i = 0; i < 15; i++) {
    newStrand.push(returnRandBase())
  }
  return newStrand
}

const pAequorFactory= (num,arr)=>{
  return{
    specimenNum:num,
    dna:arr,
    mutate(){
      let randomIndex=Math.floor(Math.random()*this.dna.length());
      let randomBase=returnRandBase();
      while(dna[randomIndex]==randomeBase){
        randomBase=returnRandBase();
      }
      dna[randomIndex]=randomBase;
    },
    compareDNA(pAequor){
      let ex1=pAequor.dna;
      let ex2=this.dna;
      let sumForMatch=0;
      for(let i=0;i<pAequor.dna.length;i++){
        if(ex2[i]==ex1[i]){
          sumForMatch++;
        }
      }
      const matchPrecentage=((sumForMatch /pAequor.dna.length)*100).toFixed(0);
      console.log("Specimen #"+pAequor.specimenNum+" and specimen #"+this.specimenNum+" have "+matchPrecentage+"% DNA in common");


    },
    willLikelySurvive(){
      let sumForMatch=0;
      for(let i=0;i<this.dna.length;i++){
        if(this.dna[i]=='C'||this.dna[i]=='G'){
          sumForMatch++;
        }
      }
      const matchPrecentage=((sumForMatch /this.dna.length)*100).toFixed(0);
      if(matchPrecentage>=60){
        return true;
      }
      else return false;
    }

  }

}
let objArr=[];
let arrWillLikelySurvive=[]
for(let i=0;i<100;i++){
objArr.push(pAequorFactory(i+1,mockUpStrand()));
if(objArr[i].willLikelySurvive()){
arrWillLikelySurvive.push(objArr[i]);}
}
console.log(arrWillLikelySurvive);


