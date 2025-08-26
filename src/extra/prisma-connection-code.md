npm install prisma --dev

npm i @prisma/client

npx prisma init

//inside lib, make a file name db.ts
```
import {PrismaClient} from "@prisma/client"
const globalFormPrisma = globalThis as unknown as { prisma: PrismaClient }
export const db = globalForPrisma.prisma || new PrismaClient()
if(process.env.NODE_ENV !== "production") globalForPrisma.prisma = db
```
// initialize a model

npx prisma generate

npx prisma db push

