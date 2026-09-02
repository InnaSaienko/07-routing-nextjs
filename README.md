# Note HUB

Note HUB is a notes management application built with Next.js 16 that demonstrates various routing techniques including intercepting routes, parallel routes, and dynamic routing.

## About the Project

This project showcases Next.js 16 App Router features through a practical notes application. It implements different routing patterns to create a seamless user experience with modal dialogs, filtering, and note management.

## Technologies Used

- **Next.js 16** with App Router
- **React 19** with TypeScript
- **CSS Modules** for styling
- **React Query** for data fetching
- **Axios** for API calls
- **Formik + Yup** for form handling
- **React Paginate** for pagination

## Routing Features Demonstrated

### Intercepting Routes
- Modal dialogs that intercept navigation using `(.)` prefix
- Note preview modal that appears when clicking note links

### Parallel Routes
- Simultaneous rendering of notes content and sidebar filters
- Independent route handling within the same layout

### Dynamic Routes
- Note filtering by tags using catch-all routes `[...slug]`
- Individual note pages with dynamic `[id]` parameters

### Route Groups
- Organized folder structure using `(group)` naming convention
- Clean URL structure without affecting routing

## Project Structure

```
app/
├── @modal/(.)notes/[id]/    # Intercepting route for note preview modal
├── notes/
│   ├── filter/
│   │   ├── @sidebar/        # Parallel route for filter sidebar
│   │   └── [...slug]/       # Dynamic filtering routes
│   └── [id]/                # Individual note pages
├── layout.tsx
└── page.tsx

components/
├── Modal/                   # Reusable modal component
├── Header/
├── Footer/
└── TanStackProvider/        # React Query provider
```

## Getting Started

Run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) to see the application.

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

## Key Features

- **Note Management**: Create, read, update, and delete notes
- **Tag Filtering**: Filter notes by tags with dynamic routing
- **Modal Previews**: Click on notes to see previews in modal dialogs
- **Search**: Debounced search functionality
- **Pagination**: Navigate through notes with pagination

## Learn More About Next.js

- [Next.js Documentation](https://nextjs.org/docs)
- [Next.js Learn Course](https://nextjs.org/learn)
- [Next.js GitHub Repository](https://github.com/vercel/next.js)

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new) from the creators of Next.js.
