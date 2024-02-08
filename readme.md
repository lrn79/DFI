# How to run project 


```
Open your terminal
npm install
after run your project
npm run dev
```


---card---
import { useState } from 'react';
import img from '../img/DFI-Logo.png'
const message = () => {
    const [cards] = useState([
        {
            title: "Card-1",
            name: 'sadekul islam',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. pariatur dolorum molestias veniam!'
        },
        {
            title: "Card-2",
            name: 'sadekul islam',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. pariatur dolorum molestias veniam!'
        },
        {
            title: "Card-3",
            name: 'sadekul islam',
            text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. pariatur dolorum molestias veniam!'
        }
    ])
    return (
        <div className="">
            <div className="text-center py-10">
                <h1>Messages</h1>
            </div>
            <div className='grid lg:grid-cols-4 sm:grid-cols-12 gap-10 ml-52 '>
                {
                    cards.map((card, i) => (


                        <div key={i} className="bg-black p-8 pr-6  rounded-xl  ">
                            <img src={img} alt="" className='h-20 mx-auto' />
                            <h4 className='uppercase text-xl font-bold'>{card.name}</h4>
                            <p className='text-sm leading-7 my-3'>Lorem ipsum dolor sit amet consectetur adipisicing elit. pariatur dolorum molestias veniam!</p>
                            <button className='bg-btn_primary py-2.5 px-2 rounder-full'> see more</button>
                        </div>
                    ))
                }
            </div>

        </div>
    );
};

export default message;